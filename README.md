#Cho 4 điểm. Lập biểu thức kiểm tra xem đó là tứ giác lồi hoặc lõm.
#Vẽ tứ giác đó với màu bất kỳ nhập từ bàn phím
#Hướng giải quyết: Kiểm tra 4 điểm có tạo thành tứ giác hay không(không có 3 điểm nào thẳng hàng), 
#Input
import math
import turtle
#Lấy dữ liệu
xa=int(input('Nhập Tọa độ x của điểm A= '))
ya=int(input('Nhập Tọa độ y của điểm A= '))
xb=int(input('Nhập Tọa độ x của điểm B= '))
yb=int(input('Nhập Tọa độ y của điểm B= '))
xc=int(input('Nhập Tọa độ x của điểm C= '))
yc=int(input('Nhập Tọa độ y của điểm C= '))
xd=int(input('Nhập Tọa độ x của điểm D= '))
yd=int(input('Nhập Tọa độ x của điểm D= '))
#Tính độ dài các cạnh
AB=math.sqrt((xb-xa)**2+(yb-ya)**2)
BC=math.sqrt((xc-xb)**2+(yc-yb)**2)
AC=math.sqrt((xc-xa)**2+(yc-ya)**2)
CD=math.sqrt((xd-xc)**2+(yd-yc)**2)
DA=math.sqrt((xa-xd)**2+(ya-yd)**2)
BD=math.sqrt((xd-xb)**2+(yd-yb)**2)
#Tính các góc cos(x)
cosA=(AB**2+DA**2-BD**2)/(2*AB*DA)
cosB=(AB**2+BC**2-AC**2)/(2*AB*BC)
cosC=(BC**2+CD**2-BD**2)/(2*BC*CD)
cosD=(DA**2+CD**2-AC**2)/(2*DA*CD)

tugiacloi= (cosA>-1 and cosA<1) and (cosB>-1 and cosB<1) and (cosC>-1 and cosC<1) and (cosD>-1 and cosD<1)
print('Tứ giác lồi: ', tugiacloi)

color=input('Màu: ')
import turtle 
t=turtle.Turtle()
t.shape()
t.pensize(1)
t.pencolor(color)
t.penup()
t.goto(xa,ya)
t.pendown()
t.goto(xb,yb)
t.goto(xc,yc)
t.goto(xd,yd)
t.goto(xa,ya)

turtle.done()
Nhập Tọa độ x của điểm A= -120
Nhập Tọa độ y của điểm A= 130
Nhập Tọa độ x của điểm B= 140
Nhập Tọa độ y của điểm B= 150
Nhập Tọa độ x của điểm C= 160
Nhập Tọa độ y của điểm C= -170
Nhập Tọa độ x của điểm D= -180
Nhập Tọa độ x của điểm D= -190
Tứ giác lồi:  True
Màu: red
