# EXP 1 A : COMPUTATION OF DFT USING DIRECT AND FFT

# AIM: 

# To Obtain DFT and FFT of a given sequence in SCILAB. 

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
        clear;
    xn=[1 2 3 4 4 3 2 1];
    n1=0:1:length(xn)-1;
    subplot(3,1,1);
    plot2d3(n1,xn);
    xlabel('Time n');
    ylabel('Amplitude xn');
    title('Input Sequence');
    j=sqrt(-1);
    N=length(xn);
    Xk=zeros(1,N);
        for k=0:N-1;
        for n=0:N-1;  
        Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N);
        end
    end
    disp(Xk)
    K1=0:1:length(Xk)-1;
    magnitude=abs(Xk)
    subplot(3,1,2);
    plot2d3(K1,magnitude);
    xlabel('frequency(Hz)');
    ylabel('magnitude(gain)');
    title('magnitude spectrum');
    angle=atan(imag(Xk),real(Xk))
    subplot(3,1,3);
    plot2d3(K1,angle);
    xlabel('frequency(Hz)');
    ylabel('Phase');
    title('Phase spectrum');

# OUTPUT: 
<img width="756" height="715" alt="image" src="https://github.com/user-attachments/assets/7bde975d-fa91-4a6b-b498-ed85ddb908b3" />


# RESULT: 
Thus, DFT using direct method for two given sequences were performed and its result was verified.
