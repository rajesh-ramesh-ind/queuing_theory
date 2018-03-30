#MARKOVIAN QUEUES -BIRTH AND DEATH PROCESS -SINGLE SERVER AND MULTIPLE SERVER QUEUING MODEL MODELS-LITTLE'S FORMULA
#This source file is programmed BY RAJESH RAMESH for study purpose
#this program is used to calculate traffc intensity,effective arrival rate,
#Ls,Lq,Ws,Wq of a model
#This is a version 1 source code made by RAJESH RAMESH
import math as m
print("\n")
print("***************************Queueing MOdels******************************")
print("\t Make sure all the inputs are in same units")
server=int(input("Number of servers:"))
capacity=int(input("Total capacity (if infinity enter 1) :"))
a_r=0
a_t=0
s_r=0
s_t=0
print("\n")
if server==1 and capacity==1:#									model I
	print("The given model is identified as (M/M/1):(@%/FIFO)")
	print("\n")
	check=input("Is the input values are in fractions ? (y/n):")
	if check is 'y':
		print("Enter the arrival rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		a_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			a_t=round(nume/deno,3)
			a_r=round(1/a_t,3)
		print("Enter the Service rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		s_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			s_t=round(nume/deno,3)
			s_r=round(1/s_t,3)
	if check is 'n':
		a_r=float(input("Enter the arrival rate :"))
		if a_r==0:
			a_t=float(input("Enter the arrival time :"))
			a_r=(1/a_t)
		s_r=float(input("Enter the service rate :"))
		if s_r==0:
			s_t=float(input("Enter the service time :"))
			s_r=(1/s_t)
	t_i=a_r/s_r
	lists=0
	p0=round(1-t_i,3)
	ls=round(t_i/(1-t_i),3)
	lq=round(ls-t_i,3)
	ws=round(ls/a_r,3)
	wq=round(lq/a_r,3)
	t_ii=0
if server>1 and capacity==1:#									model II
	print("The given model is identified as (M/M/s):(@%/FIFO)")
	print("\n")
	checks=input("Is the input values are in fractions ? (y/n):")
	if checks is 'y':
		print("Enter the arrival rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		a_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			a_t=round(nume/deno,3)
			a_r=round(1/a_t,3)
		print("Enter the Service rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		s_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			s_t=round(nume/deno,3)
			s_r=round(1/s_t,3)
	if checks is 'n':
		a_r=float(input("Enter the arrival rate:"))
		if a_r==0:
			a_t=float(input("Enter the arrival time:"))
			a_r=(1/a_t)
		s_r=float(input("Enter the service rate:"))
		if s_r==0:
			s_t=float(input("Enter the service time:"))
			s_r=(1/s_t)
	t_i=round(a_r/(server*s_r),3)
	lists=0
	p1=0
	for i in range(0,server):
		p1=p1+m.pow(server*t_i,i)/m.factorial(i)
	p2=round(m.pow(server*t_i,server)/m.factorial(server),3)
	p3=round(m.pow(1-t_i,-1),3)
	p0=round(1/(p1+(p2*p3)),3)
	ls1=t_i/m.pow(1-t_i,2)
	ls2=m.pow(server*t_i,server)/m.factorial(server)
	ls=(round(ls1,3)*round(ls2,3)*p0)+server*t_i
	lq=ls-(a_r/s_r)
	ws=ls/a_r
	wq=lq/a_r
	t_ii=0
if server==1 and capacity>1:#									model III
	print("The given model is identified as (M/M/1):(k/FIFO)")
	print("\n")
	check1=input("Is the input values are in fractions ? (y/n):")
	if check1 is 'y':
		print("Enter the arrival rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		a_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			a_t=round(nume/deno,3)
			a_r=round(1/a_t,3)
		print("Enter the Service rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		s_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			s_t=round(nume/deno,3)
			s_r=round(1/s_t,3)
	if check1 is 'n':
		a_r=float(input("Enter the arrival rate:"))
		if a_r==0:
			a_t=float(input("Enter the arrival time:"))
			a_r=(1/a_t)
		s_r=float(input("Enter the service rate:"))
		if s_r==0:
			s_t=float(input("Enter the service time:"))
			s_r=(1/s_t)
	t_i=round(a_r/s_r,3)
	lists=0
	p0=round((1-t_i)/(1-m.pow(t_i,capacity+1)),3)
	t_ii=round(s_r*(1-p0),3)
	ls1=round(t_i/(1-t_i),3)
	ls2=round((capacity+1)*m.pow(t_i,capacity+1),3)
	ls3=round(1-(m.pow(t_i,capacity+1)),3)
	ls=round(ls1-(ls2/ls3),3)
	lq=round(ls-(t_ii/s_r),3)
	ws=round(ls/t_ii,3)
	wq=round(lq/t_ii,3)
if server>1 and capacity>1:#									model IV
	print("The given model is identified as (M/M/S):(k/FIFO)")
	print("\n")
	check1=input("Is the input values are in fractions ? (y/n):")
	if check1 is 'y':
		print("Enter the arrival rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		a_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			a_t=round(nume/deno,3)
			a_r=round(1/a_t,3)
		print("Enter the Service rate:")
		nume=int(input("Numerator:"))
		deno=int(input("Denominator:"))
		s_r=round(nume/deno,3)
		if nume and deno is 0:
			print("Enter the arrival time:")
			nume=int(input("Numerator:"))
			deno=int(input("Denominator:"))
			s_t=round(nume/deno,3)
			s_r=round(1/s_t,3)
	if check1 is 'n':
		a_r=float(input("Enter the arrival rate:"))
		if a_r==0:
			a_t=float(input("Enter the arrival time:"))
			a_r=(1/a_t)
		s_r=float(input("Enter the service rate:"))
		if s_r==0:
			s_t=float(input("Enter the service time:"))
			s_r=(1/s_t)
	t_i=round(a_r/(server*s_r),3)
	z=0
	for n in range(0,server):
		z=z+(m.pow(server*t_i,n)/m.factorial(n))
	y=0
	for l in range(0,capacity-server+1):
		y=y+m.pow(t_i,l)
	h=z+(m.pow(server*t_i,server)/m.factorial(server))*y
	p0=round(1/h,3)
	lists=1
	pn=[p0]
	for n in range(1,capacity+1):
		if n>0 and n<=server:
			value=(m.pow(server*t_i,n)/m.factorial(n))*p0
			pn.append(round(value,3))
		if n>server and n<=capacity:
			value1=(m.pow(server*t_i,server)/m.factorial(server))*p0*m.pow(t_i,n-server)
			pn.append(round(value1,3))
	g=0
	for n in range(0,server):
		g=g+(round((server-n)*pn[n],3))
	t_ii=s_r*(server-g)
	ls=0
	for n in range(0,capacity+1):
		ls=ls+(n*pn[n])
	lq=ls-(t_ii/s_r)
	ws=ls/t_ii
	wq=lq/t_ii
print("\n")
print("RESULT:")
print("\n")
print("Mean arrival rate",a_r)
print("Mena service rate",s_r)
print("Traffic intensity =",t_i)
if not t_ii==0:
	print("The effective arrival rate=",round(t_ii,3))
if lists is 1:
	for n in range(0,capacity+1):
		print("p",n,"=",pn[n])
else:
	print("p",n,"=",p0)	
print("Average number of objects in the system:",round(ls,3))
print("Average number of objects in the queue:",round(lq,3))
print("Average number of waiting time in the system:",round(ws,3))
print("Average number of waiting time in the queue:",round(wq,3))
