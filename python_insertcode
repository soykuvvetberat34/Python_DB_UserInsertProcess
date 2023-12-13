import pymysql.cursors
def insert(name,surname,age,city):
    mydb=pymysql.connect(
        host="localhost",
        user="root",
        password="34.bjkberat",
        database="beratsoykuvvet"
    )
    mycursor=mydb.cursor()
    sql="INSERT INTO users(name,surname,age,city) VALUE(%s,%s,%s,%s)"
    values=(name,surname,age,city) 
    mycursor.execute(sql,values)
    
    try:
         mydb.commit()  
         print("User created..")
    except pymysql.connect.Error as err:
        print("error:",err)
    finally:
        mydb.close()
        print("Database closed..")



name1=input("Enter your name:")
surname1=input("Enter your surname:")
age1=int(input("Enter your age:"))
city1=input("Enter your city:")
insert(name1,surname1,age1,city1)
