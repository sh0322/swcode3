```python
a = [10,20,30]
a[3]
```


    ---------------------------------------------------------------------------

    IndexError                                Traceback (most recent call last)

    Input In [1], in <cell line: 2>()
          1 a = [10,20,30]
    ----> 2 a[3]
    

    IndexError: list index out of range



```python
n = int('20%')
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    Input In [2], in <cell line: 1>()
    ----> 1 n = int('20%')
    

    ValueError: invalid literal for int() with base 10: '20%'



```python
a = 100 + '200'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Input In [3], in <cell line: 1>()
    ----> 1 a = 100 + '200'
    

    TypeError: unsupported operand type(s) for +: 'int' and 'str'



```python
try:
    a = [10,20,30]
    a[3]
except Exception as e:
    print(e)
```

    list index out of range
    


```python
try:
    n = int('20%')
except Exception as e:
    print(e)
```

    invalid literal for int() with base 10: '20%'
    


```python
try:
    a = 100 +'200'
except Exception as e:
    print(e)
```

    unsupported operand type(s) for +: 'int' and 'str'
    


```python
a = [1,2,3,4,5]
b = ['첫 번째','두 번째','세 번째','네 번쨰','다섯 번째']
n = int(input('a의 요소를 하나 선택하시오 : '))
print('{}은(는) {} 요소입니다.'.format(n,b[a.index(n)]))
```

    a의 요소를 하나 선택하시오 : 2
    2은(는) 두 번째 요소입니다.
    


```python
a = [1,2,3,4,5]
b = ['첫 번째','두 번째','세 번째','네 번쨰','다섯 번째']
try:
    n = int(input('a의 요소를 하나 선택하시오 : '))
except:
    print('오류 값이 정수나 실수가 아님')
else:
    print('{}은(는) {} 요소입니다.'.format(n,b[a.index(n)]))
```

    a의 요소를 하나 선택하시오 : 삼
    오류 값이 정수나 실수가 아님
    


```python
f = open('numbers.txt','w')
f.write('100\n200\n300\n400')
f.close()
f = open('numbers.txt','r')
s = f.read()
print(s)
f.close()
```

    100
    200
    300
    400
    


```python
f = open('we_will_rock.txt','w')
f.write('''Buddy, you\'re a boy, make a bog noise\nPlaying in the street, gonna be a big man someday
you got mud on your face, you big disgrace
Kicking your can all over thr place,singin\'
We will, we will rock you
We will, we will rock you''')

f.close()
f = open('we_will_rock.txt','r')
s = f.read()
print(s)
f.close()
```

    Buddy, you're a boy, make a bog noise
    Playing in the street, gonna be a big man someday
    you got mud on your face, you big disgrace
    Kicking your can all over thr place,singin'
    We will, we will rock you
    We will, we will rock you
    


```python
f = open('numbers.txt','w')
f.write('100\n200\n300\n400')
f.close()
f = open('numbers.txt','r')
for i in range(4):
    s = f.readline().rstrip()
    print(s)
f.close()
```

    100
    200
    300
    400
    


```python
f = open('we_will_rock.txt','w')
f.write('''Buddy, you\'re a boy, make a bog noise
Playing in the street, gonna be a big man someday 
you got mud on your face, you big disgrace
Kicking your can all over thr place,singin\'
We will, we will rock you
We will, we will rock you''')
f.close()
f = open('we_will_rock.txt','r')
for i in range(6):
    s = f.readline().rstrip()
    print(s)
f.close()
```

    Buddy, you're a boy, make a bog noise
    Playing in the street, gonna be a big man someday
    you got mud on your face, you big disgrace
    Kicking your can all over thr place,singin'
    We will, we will rock you
    We will, we will rock you
    


```python
f = open('we_will_rock.txt','w')
f.write('''Buddy, you\'re a boy, make a bog noise
Playing in the street, gonna be a big man someday 
you got mud on your face, you big disgrace
Kicking your can all over thr place,singin\'
We will, we will rock you
We will, we will rock you''')
f.close()
import sys
fname = input('입력할 파일의 이름 : ')
try:
    f = open(fname,'r',encoding = 'UTF8')
except IOError:
    print('Could not read file:',fname)
    sys.exit()
except:
    print('Unexcepted error:',sys.exc_info()[0])
    sys.exit()
n = 1
I = f.readline().rstrip().upper()
while I:
    print(I)
    I = f.readline().rstrip().upper()
f.close()
    
```

    입력할 파일의 이름 : we_will_rock.txt
    BUDDY, YOU'RE A BOY, MAKE A BOG NOISE
    PLAYING IN THE STREET, GONNA BE A BIG MAN SOMEDAY
    YOU GOT MUD ON YOUR FACE, YOU BIG DISGRACE
    KICKING YOUR CAN ALL OVER THR PLACE,SINGIN'
    WE WILL, WE WILL ROCK YOU
    WE WILL, WE WILL ROCK YOU
    


```python
f = open('we_will_rock.txt','w')
f.write('''Buddy, you\'re a boy, make a bog noise
Playing in the street, gonna be a big man someday 
you got mud on your face, you big disgrace
Kicking your can all over thr place,singin\'
We will, we will rock you
We will, we will rock you''')
f.close()

import sys
fname = input('입력할 파일의 이름 : ')
try:
    f = open(fname,'r',encoding = 'UTF8')
except IOError:
    print('Could not read file:',fname)
    sys.exit()
except:
    print('Unexcepted error:',sys.exc_info()[0])
    sys.exit()
    
I = f.readline().rstrip()
l2 = []
n =0

while I:
    l2.append(I)
    I = f.readline().rstrip()
    n += 1
for i in range(n-1,-1,-1):
    print(l2[i])
f.close()
```

    입력할 파일의 이름 : we_will_rock.txt
    We will, we will rock you
    We will, we will rock you
    Kicking your can all over thr place,singin'
    you got mud on your face, you big disgrace
    Playing in the street, gonna be a big man someday
    Buddy, you're a boy, make a bog noise
    


```python

```
