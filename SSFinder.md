#SSFinder cdoe is develoved by Dr. Santosh K Upadhyay and Dr. Shailesh Sharma (unpublished).

#!/usr/bin/python
import commands
import time
start = time.time()
dir\_name = raw\_input('Give the address of your working directory \n') + '/'
file\_1 = raw\_input('Give the file name in FASTA format containing sequences \n')
output\_format = raw\_input('Please select the output format from these 3 [.txt,.xls,.csv] \n')
##output\_format = '.xls'
to\_write\_1 = open(dir\_name+'SSFinder-output'+output\_format,'w')
array = [.md](.md)
a = open(dir\_name+file\_1, 'r').readlines()
for index in range(len(a)):
> if a[index](index.md).startswith('>'):
> > array.append(index)
array.append(len(a))
constant = [.md](.md)
##print 'Contig\tCondition\tCrisper-Site\tStart\tEnd'
to\_write\_1.write(('%s\t%s\t%s\t%s\t%s\t%s\t%s\n')%('Identifier','Condition','CRISPR-Target Site with NGG PAM','Start','End','Condition with seed sequence','Specific CRISPR-Taget Site'))
for index in range(len(array)-1):

> All = 0
> sel = 0
> > str = ''
> > for element in range(array[index](index.md)+1,array[index+1]):
> > > str+=a[element](element.md).strip()
##	print str[0:23],len(str[0:23])

> for slice in range(0,(len(str)/len(str[0:23]))**23):
##		string = [.md](.md)
> > if len(str[slice:23+slice]) == 23 and str[slice:23+slice][21](21.md) == 'G' and str[slice:23+slice][22](22.md) == 'G' and (str[slice:23+slice][0](0.md) == 'G' or str[slice:23+slice][0](0.md) == 'C') and (str[slice:23+slice][19](19.md) == 'G' or str[slice:23+slice][19](19.md) == 'C'):
> > > string = [.md](.md)
##			print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','G or CN18G or C','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23
##			to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'G or CN18G or C',str[slice:23+slice],slice+1,slice+23))
> > > string.append(a[array[index](index.md)].strip())
> > > string.append('G or CN18G or C')
> > > string.append(str[slice:23+slice])
> > > string.append(slice+1)
> > > string.append(slice+23)
> > > All = All + 1
##			print 'ALL', str[slice:23+slice],'MAKE THIS AS CONSTANT',str[slice+8:23+slice]
> > > constant.append(str[slice+8:23+slice])
> > > if constant.count(str[slice+8:23+slice]) == 1:
##				print 'WE GOT IT', str[slice:23+slice]
> > > > print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','G or CN7S11G or C','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23##,'TO GREP',str[slice+8:23+slice]
##				to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'G or CN7S11G or C',str[slice:23+slice],slice+1,slice+23))
> > > > sel = sel + 1
##				string += a[array[index](index.md)].split('>')[1](1.md).strip()+'\t'+'G or CN7S11G or C'+'\t'+str[slice:23+slice]+'\t'+str(slice+1)+'\t'+str(slice+23)
##				string.append(a[array[index](index.md)])
> > > > string.append('G or CN7S11G or C')
> > > > string.append(str[slice:20+slice])

> > > for e in string:
> > > > to\_write\_1.write(('%s\t')%(e))

> > > to\_write\_1.write('\n')**


> elif len(str[slice:23+slice]) == 23 and str[slice:23+slice][21](21.md) == 'G' and str[slice:23+slice][22](22.md) == 'G' and (str[slice:23+slice][0](0.md) == 'A' or str[slice:23+slice][0](0.md) == 'T') and (str[slice:23+slice][19](19.md) == 'A' or str[slice:23+slice][19](19.md) == 'T'):
> > string = [.md](.md)
> > > print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','A or TN18A or T','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23
##			to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'A or TN18A or T',str[slice:23+slice],slice+1,slice+23))

> > string.append(a[array[index](index.md)].strip())
> > > string.append('A or TN18A or T')
> > > string.append(str[slice:23+slice])
> > > string.append(slice+1)
> > > string.append(slice+23)

> > All = All + 1
> > constant.append(str[slice+8:23+slice])
> > > if constant.count(str[slice+8:23+slice]) == 1:
##                              print 'WE GOT IT', str[slice:23+slice]
> > > > print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','A or TN7S11A or T','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23##,'TO GREP',str[slice+8:23+slice]
##				to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'A or TN7S11A or T',str[slice:23+slice],slice+1,slice+23))
> > > > sel = sel + 1
> > > > string.append('A or TN7S11A or T')
> > > > string.append(str[slice:20+slice])

> > > for e in string:
> > > > to\_write\_1.write(('%s\t')%(e))

> > > to\_write\_1.write('\n')

> elif len(str[slice:23+slice]) == 23 and str[slice:23+slice][21](21.md) == 'G' and str[slice:23+slice][22](22.md) == 'G' and (str[slice:23+slice][0](0.md) == 'G' or str[slice:23+slice][0](0.md) == 'C') and (str[slice:23+slice][19](19.md) == 'A' or str[slice:23+slice][19](19.md) == 'T'):
> > string = [.md](.md)
##                      print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','G or CN18A or T','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23
##			to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'G or CN18A or T',str[slice:23+slice],slice+1,slice+23))
> > > string.append(a[array[index](index.md)].strip())
> > > string.append('G or CN18A or T')
> > > string.append(str[slice:23+slice])
> > > string.append(slice+1)
> > > string.append(slice+23)

> > All = All + 1
> > > constant.append(str[slice+8:23+slice])
> > > if constant.count(str[slice+8:23+slice]) == 1:
##                              print 'WE GOT IT', str[slice:23+slice]
> > > > print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','G or CN7S11A or T','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23##,'TO GREP',str[slice+8:23+slice]
##				to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'G or CN7S11A or T',str[slice:23+slice],slice+1,slice+23))
> > > > sel = sel + 1
> > > > string.append('G or CN7S11A or T')
> > > > string.append(str[slice:20+slice])

> > > for e in string:
> > > > to\_write\_1.write(('%s\t')%(e))

> > > to\_write\_1.write('\n')

> elif len(str[slice:23+slice]) == 23 and str[slice:23+slice][21](21.md) == 'G' and str[slice:23+slice][22](22.md) == 'G' and (str[slice:23+slice][0](0.md) == 'A' or str[slice:23+slice][0](0.md) == 'T') and (str[slice:23+slice][19](19.md) == 'G' or str[slice:23+slice][19](19.md) == 'C'):
> > string = [.md](.md)
##                      print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','A or TN18G or C','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23
##			to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'A or TN18G or C',str[slice:23+slice],slice+1,slice+23))
> > > string.append(a[array[index](index.md)].strip())
> > > string.append('A or TN18G or C')
> > > string.append(str[slice:23+slice])
> > > string.append(slice+1)
> > > string.append(slice+23)

> > All = All + 1
> > constant.append(str[slice+8:23+slice])
> > > if constant.count(str[slice+8:23+slice]) == 1:
##                              print 'WE GOT IT', str[slice:23+slice]
> > > > print a[array[index](index.md)].split('>')[1](1.md).strip(),'\t','A or TN7S11G or C','\t',str[slice:23+slice],'\t',slice+1,'\t',slice+23##,'TO GREP',str[slice+8:23+slice]
##				to\_write\_1.write(('%s\t%s\t%s\t%d\t%d\n')%(a[array[index](index.md)].split('>')[1](1.md).strip(),'A or TN7S11G or C',str[slice:23+slice],slice+1,slice+23))
> > > > sel = sel + 1

> > > string.append('A or TN7S11G or C')
> > > > string.append(str[slice:20+slice])
> > > > for e in string:
> > > > > to\_write\_1.write(('%s\t')%(e))

> > > > to\_write\_1.write('\n')

> print 'Total number of CRISPER TARGET SITES IN ',a[array[index](index.md)].split('>')[1](1.md).strip(),' are ',All, ' Selected are ',sel
> to\_write\_1.write(('%s\t%s\t%s\t%d\t%s\t%d\n')%('Total number of CRISPER SITES IN ',a[array[index](index.md)].split('>')[1](1.md).strip(),' are ',All,' Selected are ',sel))
print 'time is',time.time()-start
print 'NOW IT COMPLETES'