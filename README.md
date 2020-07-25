# Important and basic Functions of statistics used in data analysis:-

1. Mean
2. Median
3. Mode
4. Variance
5. Standard deviation


## 1. Mean
Fucntion for mean 

    def mean1(list):
        mean1=sum(list)/len(list)
        return mean1
    
Example

    list=[1,2,3,4]
    Mean=mean1(list)
    Mean
Output

    2.5
        
## 2. Median

Function for median

    def median1(list):
        l=len(list)
        s=sorted(list)
        if l % 2 == 0:
           median1=(s[l//2]+s[l//2 - 1])/2
        else:
           median1=s[l//2]
    return median1
Example

    list1=[6,8,3,4,5,1]
    m=median1(list1)
    m

output

    4.5
    
## 3. Mode

Function for mode

    def mode1(list):
        s=sorted(list)
        l1=[]
        i = 0
        while i < len(list) : 
            l1.append(s.count(s[i])) 
            i += 1
            d1 = dict(zip(s, l1)) 
            d2={k for (k,v) in d1.items() if v == max(l1) } 
        print("Mode(s) is/are :" + str(d2))

Example

    l=[11,11,11,2,3,2,2,2,4,5,11,6,8,8,8,8]
    m=mode1(l)
    m

Output

    Mode(s) is/are :{8, 2, 11}

## 4. Variance

Function for variance

    def variance1(list):
        m=sum(list)/len(list)
        var= sum((i - m) ** 2 for i in list) / len(list) 
        print("The variance of list is : " + str(var))

Example
    
    l=[1,2,3]
    v=variance1(l)
   
Output

    The variance of list is : 0.6666666666666666

## 5. Standard Deviation

Function for Standard Deviation
    
    def stdev1(list):
        m=sum(list)/len(list)
        var= sum((i - m) ** 2 for i in list) / len(list) 
        stdev=var**0.5
        print("The standar deviation  of list is : " + str(stdev))
        
Example
    
    l=[1,2,3]
    st=stdev1(l)
   
Output

    The standar deviation  of list is : 0.816496580927726
