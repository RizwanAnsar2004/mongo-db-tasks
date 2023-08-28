# mongo-db-tasks



**TO CREATE COLLECTION:**

use Rizwan
db.createCollection("Rizwan")


**TO CREATE RECORD OF FIVE STUDENTS:**


db.Student.insertMany(


[
{
studentId:1,firstName:"rizwan",lastName:"ansar",age:18,subjects:["FOP","OOP","DSA","DBMS"],address:{street:"dalmia",city:"karachi",zipCode:75260,state:"pakistan"}},


{studentId:2,firstName:"sarwan",lastName:"tanweer",age:19,subjects:["FOP","OOP"],address:{street:"highway",city:"karachi",zipCode:75360,state:"pakistan"}},


{studentId:3,firstName:"ahsan",lastName:"qadri",age:19,subjects:["FOP","OOP","DBMS"],address:{street:"cant",city:"karachi",zipCode:75460,state:"pakistan"}},


{studentId:4,firstName:"buland",lastName:"bakht",age:18,subjects:["FOP"],address:{street:"jouhar",city:"karachi",zipCode:75560,state:"pakistan"}},


{studentId:5,firstName:"izaan",lastName:"aktar",age:20,subjects:["DSA","DBMS"],address:{street:"shah faisal",city:"karachi",zipCode:75660,state:"pakistan"}


}
])


**result:**


{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("64ed0cc50d30dbd4dc79f95a"),
    '1': ObjectId("64ed0cc50d30dbd4dc79f95b"),
    '2': ObjectId("64ed0cc50d30dbd4dc79f95c"),
    '3': ObjectId("64ed0cc50d30dbd4dc79f95d"),
    '4': ObjectId("64ed0cc50d30dbd4dc79f95e")
  }
}


![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/89e24672-10ee-4759-b9b2-c039b3bd75ad)


**TASK 2: TO RETRIEVE DATA OF ALL STUDENTS:**

db.Student.find({})


**result:**  

![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/756a6b5c-e4c7-424b-9c48-fdf9992ec210)
![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/6e4b0842-09d2-4330-9636-275f745c34fe)
![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/b4339d97-c05d-4db1-bd94-7fe8241c4316)


TO RETRIVE A STUDENT FROM ITS ID:

db.Student.find({studentId:1})


**result**


![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/e9494421-7ac7-4085-aca5-256085599cea)


**Retrieve students whose age is greater than a certain value (e.g., 20)**.


db.Student.find({age:{$lt:19}})

**result:**
![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/42a08542-2847-4090-89fe-7babfd8b358c)


**Retrieve students who are enrolled in a specific subject (use an array query operator)**.


db.Student.find({ subjects: { $elemMatch: { $eq: "OOP" } } })

![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/2277ee0d-e8c1-4165-8b25-852e06a3d6d9)
![image](https://github.com/RizwanAnsar2004/mongo-db-tasks/assets/131580981/9e793a4f-b9e6-4e9c-a718-2fe1490a236a)
