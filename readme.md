exp 2 part 1
```
%sin wave
t=0:0.005:10;
f=1;
x1=sin(2*pi*f*t);
subplot(5,2,1);
plot(t,x1);
xlabel('time');
ylabel('amplitude');
title('sin signal')
%cos wave
t=0:0.005:10;
f=1;
x2=cos(2*pi*f*t);
subplot(5,2,2);
plot(t,x2);
xlabel('time');
ylabel('amplitude');
title('cos signal')
%cot signal
t=0:0.005:10;
f=1;
x3=cot(2*pi*f*t);
subplot(5,2,3);
plot(t,x3);
xlabel('time');
ylabel('amplitude');
title('cot signal')
%sininverse fuction

%unit step signal
t=-20:.001:20;
x5=([t>=0]);
subplot(5,2,5);
plot(t,x5);
axis([-20 20 -2 2]);
xlabel('time');
ylabel('amplitude');
title('unit step signal')

n= -3:0.05:3
x5=sawtooth(n);
subplot(5,2,5);
plot(n,x5);
xlabel('time');
ylabel('amplitude');
title('Sawtooth Discrete Wave');


x6 = ([n==0]);
subplot(5,2,6);
plot(n,x6);
axis([-2,2 -1 1]);
title('Unit Impulse Discrete Signal');
xlabel('time');
ylabel('amplitude');

x7 = ([n>=0]);
subplot(5,2,7);
plot(n,x7);
axis([-3,3 -2 2]);
title('Unit Step Discrete Signal');
xlabel('time');
ylabel('amplitude');

n = 0:0.05:2.5
x8 = n;
subplot(5,2,8);
plot(n,x8);
title('Unit Ramp Discrete Signal');
xlabel('time');
ylabel('amplitude');

n = -1:0.05:1
x9 = sinc(2*pi*f*n);
subplot(5,2,9);
plot(n,x9);
title('Sinc Function');
xlabel('time');
ylabel('amplitude');

n= -10:0.3:10
x10 = sawtooth(n,0.5);
subplot(5,2,10);
plot(n,x10);
title('Triangular Discrete Wave');
xlabel('time');
ylabel('amplitude');

```
exp 2 part 2
```
f =1 
n = -1:0.07:7
x1 = sin(2*pi*f*n);
subplot(5,2,1);
stem(n,x1);
xlabel('time');
ylabel('amplitude');
title('Sin Discrete Wave');

x2=cos(2*pi*f*n)
subplot(5,2,2);
stem(n,x2);
xlabel('time');
ylabel('amplitude');
title('Cos Discrete Wave');

n = -3:0.05:3
x3=tan(2*pi*f*n);
subplot(5,2,3);
stem(n,x3);
xlabel('time');
ylabel('amplitude');
title('Tan Discrete Wave');

n = -3:0.05:3
x4=cot(2*pi*f*n);
subplot(5,2,4);
stem(n,x4);
xlabel('time');
ylabel('amplitude');
title('Cot Discrete Wave');

n= -3:0.05:3
x5=sawtooth(n);
subplot(5,2,5);
stem(n,x5);
xlabel('time');
ylabel('amplitude');
title('Sawtooth Discrete Wave');


x6 = ([n==0]);
subplot(5,2,6);
stem(n,x6);
axis([-2,2 -1 1]);
title('Unit Impulse Discrete Signal');
xlabel('time');
ylabel('amplitude');

x7 = ([n>=0]);
subplot(5,2,7);
stem(n,x7);
axis([-3,3 -2 2]);
title('Unit Step Discrete Signal');
xlabel('time');
ylabel('amplitude');

n = 0:0.05:2.5
x8 = n;
subplot(5,2,8);
stem(n,x8);
title('Unit Ramp Discrete Signal');
xlabel('time');
ylabel('amplitude');

n = -1:0.05:1
x9 = sinc(2*pi*f*n);
subplot(5,2,9);
stem(n,x9);
title('Sinc Function');
xlabel('time');
ylabel('amplitude');

n= -10:0.3:10
x10 = sawtooth(n,0.5);
subplot(5,2,10);
stem(n,x10);
title('Triangular Discrete Wave');
xlabel('time');
ylabel('amplitude');

```
exp3
```
f=1;
t=-5:0.01:5;
x1=sin(2*pi*f*t);
subplot(5,2,1);
plot(t,x1);
title('Sin Signal');
xlabel('Time');
ylabel('Ampltude');

t=-5:0.01:5;
x2=cos(2*pi*f*t);
subplot(5,2,2);
plot(t,x2);
title('cos Signal');
xlabel('Time');
ylabel('Ampltude');


x3=x1+x2;
subplot(5,2,3);
plot(t,x3);
title('Addition Signal');
xlabel('Time');
ylabel('Ampltude');

x4=x1-x2;
subplot(5,2,4);
plot(t,x4);
title('Subtraction Signal');
xlabel('Time');
ylabel('Ampltude');

x5=x1.*x2;
subplot(5,2,5);
plot(t,x5);
title('Multiplication Signal');
xlabel('Time');
ylabel('Ampltude');


%time scaling
t1=t/2;
subplot(5,2,6);
plot(t1,x1);
axis([-10 10 -1 1]);
title('time scaling - compression');
xlabel('time');
ylabel('Amplitude');

%time scaling
t2=5*t;
subplot(5,2,7);
plot(t2,x1);
axis([-10 10 -1 1]);
title('time scaling - expansion');
xlabel('time');
ylabel('Amplitude');

%time shifting
t3=t-5;
subplot(5,2,8);
plot(t3,x1);
title('time Shifting - right');
xlabel('time');
ylabel('Amplitude');

%time shifting
t4=t+5;
subplot(5,2,9);
plot(t4,x1);
title('time Shifting - left');
xlabel('time');
ylabel('Amplitude');


%time folding
t5=-t;
subplot(5,2,10);
plot(t5, x1);
title('time folding');
xlabel('time');
ylabel('Amplitude');
```
exp 4
```
%transform of independent variable

t=-10:0.01:10;
x=sin(t);
subplot(3,2,1);
plot(t,x);
title('Sin Signal');
xlabel('Time');
ylabel('Amplitude');

%time shifting
t1=t+3;
subplot(3,2,2);
plot(t1,x);
title('Right Shifted Sin Signal');
xlabel('Time');
ylabel('Amplitude');

t2=t-3;
subplot(3,2,3);
plot(t2,x);
title('Left Shifted Sin Signal');
xlabel('Time');
ylabel('Amplitude');

%time scalling
t3=2*t;
subplot(3,2,4);
plot(t3,x);
title('Comprssed Sin Signal');
xlabel('Time');
ylabel('Amplitude');

t4=t/2;
subplot(3,2,5);
plot(t4,x);
title('Expanded Sin Signal');
xlabel('Time');
ylabel('Amplitude');

%time inversion
t5=-t;
subplot(3,2,6);
plot(t5,x);
title('Inversed Sin Signal');
xlabel('Time');
ylabel('Amplitude');
```
exp 5 part 1
```

%convolution between sequence
x1=input('Enter the first sequence');
x2=input('Enter te second sequence');
x3=conv(x1,x2);
subplot(3,2,1);
stem(x1);
title('Sequence 1');
xlabel('--n')
ylabel('Amplitude');
grid on;
subplot(3,2,2);
stem(x2);
title('Sequence 2');
xlabel('--n');
ylabel('Amplitude');
grid on;
subplot(3,2,3);
stem(x3);
title('Sequence 3');
xlabel('--n');
ylabel('Amplitude');
grid on;

%convolution between signals
t=0:0.001:2*pi;
y1=sin(t);
d1=-1:0.01:10;
y2=cos(t);
y3=conv(y1,y2);
subplot(3,2,4);
plot(y1);
title('signal 1');
xlabel('--time');
ylabel('Amplitude');
grid on;
subplot(3,2,5);
plot(y2);
title('signal 2');
xlabel('--time');
ylabel('Amplitude');
grid on;
subplot(3,2,6);
plot(x3);
title('Convolution of sequence 1&2');
xlabel('--n');
ylabel('Amplitude');
grid on;
```
exp5 part 2
```

%Deconvolution between sequence
x1=input('Enter the first sequence');
x2=input('Enter te second sequence');
x3=deconv(x1,x2);
subplot(3,2,1);
stem(x1);
title('Sequence 1');
xlabel('--n')
ylabel('Amplitude');
grid on;

subplot(3,2,2);
stem(x2);
title('Sequence 2');
xlabel('--n');
ylabel('Amplitude');
grid on;

subplot(3,2,3);
stem(x3);
title('Sequence 3');
xlabel('--n');
ylabel('Amplitude');
grid on;


%Deconvolution between signals
t=0:0.001:2*pi;
y1=sin(t);
d1=-1:0.01:10;
y2=cos(t);
y3=deconv(y1,y2);
subplot(3,2,4);
plot(y1);
title('signal 1');
xlabel('--time');
ylabel('Amplitude');
grid on;
subplot(3,2,5);
plot(y2);
title('signal 2');
xlabel('--time');
ylabel('Amplitude');
grid on;
subplot(3,2,6);
plot(x3);
title('Deonvolution of sequence 1&2');
xlabel('--n');
ylabel('Amplitude');
grid on;
```
exp8
```
syms n;
a=2;
x=a^n;
x=ztrans(x);
disp('z transform of a^n a>1');
disp(x);
syms n;
a=0.5;
x=x^n;
x1=ztrans(x);
disp('z transform of a^n 0<a<1');
disp(x1);
syms n;
a=2;
x= 1+n;
x2=ztrans(n);
disp('z transform of 1+n')
disp(x2);
A=iztrans(x);
disp('inverse z transform of a^n a>1');
disp(A);
B=iztrans(x1);
disp('inverse z transform of a^n 0<a<1');
disp(B);
C=iztrans(x2);
disp('inverse z transform of 1+n');
disp(C);
subplot(1,3,1);
zplane([1,0],[1,-2]);
subplot(1,3,2);
zplane([1,0],[1,-1/2]);
subplot(1,3,3);
zplane([1,0,0],[1,-2,1]);
```
exp9
```
t=-10:0.1:10;
T=4;
fm= 1/T;
x= cos(2*pi*fm*t);
subplot(2,2,1);
plot(t,x);
title('Continnous time signal');
xlabel('time');
ylabel('x(t)');
grid on;
n1= -10:1:10;
fs1=1.6*fm;
fs2=2*fm;
fs3=8*fm;
x1= cos(2*pi*fm/fs1*n1);
subplot(2,2,2);
stem(n1,x1);
xlabel('time');
ylabel('x(n)');
title('Discrete time signal with fs<2fm');
hold on;
subplot(2,2,2);
plot(n1,x1);
grid on;
x2= cos(2*pi*fm/fs2*n1);
subplot(2,2,3);
stem(n1,x2);
xlabel('time');
ylabel('x(n)');
title('Discrete time signal with fs= 2fm');
hold on;
subplot(2,2,3);
plot(x1,x2);
grid on;
x3= cos(2*pi*fm/fs3*n1);
subplot(2,2,4);
stem(n1,x3);
xlabel('time');
ylabel('x(n)');
title('Discrete time signal with fs>2fm');
hold on;
subplot(2,2,4);
plot(n1,x3);
grid on;
```
