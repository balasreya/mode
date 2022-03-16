# mode
#mode
print("ENTER THE NUMBER OF ELEMENTS")
x<-scan()
n<-length(x)
c<-vector()
for(i in 1:(n-1))
  {
    c[i]<-1
    c[n]<-1
for(j in (i+1):n)
      if(x[i]==x[j]) c[i]<-c[i]+1
  }
print(c)
  big=c[1];
  pos=1;
for(i in 2:n)
      if(big<c[i])
      {
      big=c[i]
      pos=i
      }
for(i in 1:n)
    if(big==c[i])
    {
      if(x[pos]<x[i])
        pos=i
    }
print("The MODE using program is")
print(x[pos])
print("The MODE using built in function is")
print(max(x[duplicated(x)]))

