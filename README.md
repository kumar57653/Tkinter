from tkinter import *


def page_2():
    k.grid_forget()
    j.grid()
def page_3():
    j.grid_forget()
    u.grid()

def page_4():
    u.grid_forget()
    a.grid()


def view_score():
    global score
    score=0
    if v.get()==3:
        score+=5
    if d.get()== 3:
        score+=5
    if z.get()==2:
        score+=5
    y.config(text="Your score: {}/15".format(score))


root = Tk()
root.configure(bg='yellow')

root.geometry('600x400')

score = 0

k = Frame(root)
k.configure(bg='yellow')
l = Label(k, text="BHUTAN'S GENERAL KNOWLEDGE", bg='yellow',font='Arial 12')
l.grid(row=0, column=0)

q = Label(k, text='What is the scientific name of Takin',bg='yellow',font='Arial 11')
q.grid(row=2, column=0)
v = IntVar()
v1 = Radiobutton(k, text='Bos grunniens', variable=v, value=1,bg='yellow')
v1.grid(row=3, column=0)
v2 = Radiobutton(k, text='Corvus brachyrhynchos', variable=v, value=2,bg='yellow')
v2.grid(row=4, column=0)
v3=Radiobutton(k,text='Budorcas taxicolor',variable=v,value=3,bg='yellow')
v3.grid(row=5,column=0)
v4=Radiobutton(k,text='Ovis aries',variable=v,value=4,bg='yellow')
v4.grid(row=6,column=0)
b = Button(k, text='NEXT', command=page_2,bg='red')
b.grid(row=10, column=0)
j1=Label(k,text='BHUTAN',height=10,width=15,bg='yellow')
j1.grid(row=11,column=0)

j = Frame(root)
j.configure(bg='darkorange')
h = Label(j, text='who is the first president of Bhutan?',font='Arial 12', bg='yellow',)
h.grid(row=0, column=1)
d = IntVar()
d1 = Radiobutton(j, text='Dr.Lotay Tsering', variable=d, value=1, bg='darkorange')
d1.grid(row=1, column=1)
d2 = Radiobutton(j, text='Tsering Tobgay', variable=d, value=2, bg='darkorange')
d2.grid(row=2, column=1)
d3=Radiobutton(j, text='Jigme Thinley', variable=d, value=3, bg='darkorange')
d3.grid(row=3, column=1)
d4=Radiobutton(j, text='Jigme Namgyel', variable=d, value=4, bg='darkorange')
d4.grid(row=4, column=1)
h = Button(j, text='NEXT', command=page_3,bg='red')
h.grid(row=5, column=1)
j2=Label(j,text='BHUTAN',height=10,width=15,bg='darkorange')
j2.grid(row=6,column=1)


u=Frame(root)
u.configure(bg='skyblue')
f=Label(u,text='when was the first election in Bhutan conducted',font='Arial 9', bg='skyblue')
f.grid(row=0,column=1)
z=IntVar()
z1=Radiobutton(u,text='2006',variable=z,value=1, bg='skyblue')
z1.grid(row=1,column=1)
z2=Radiobutton(u,text='2008',variable=z,value=2, bg='skyblue')
z2.grid(row=2,column=1)
z3=Radiobutton(u,text='2005',variable=z,value=3, bg='skyblue')
z3.grid(row=3,column=1)
z4=Radiobutton(u,text='2009',variable=z,value=4, bg='skyblue')
z4.grid(row=4,column=1)

b1=Button(u,text='Summit',command=page_4,bg='red')
b1.grid(row=5,column=1)

j3=Label(u,text='BHUTAN',height=10,width=15,bg='skyblue')
j3.grid(row=10,column=1)

a=Frame(root)
a.configure(bg='orange')
r=Label(a,text='GREAT JOB',font='Arial 12')
r.grid(row=5,column=1)

y=Button(a,text='Check your score',bg='red',command=view_score)
y.grid(row=6,column=1)
x=Label(a,text='Proud Bhutanese',bg='orange',height=30,width=50)
x.grid(row=7,column=1)
c1=Label(a,text='Bhutanese mentality',bg='orange',height=10)
c1.grid(row=8,column=1)
k.grid()

root.mainloop(
