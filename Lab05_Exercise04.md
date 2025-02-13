# Lab 5 Exercise 4

## Fields declaration and initialization


1. สร้าง console application project

```
dotnet new console --name Lab05_Ex04
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-05/assets/144197034/dc64cf74-006f-447d-94a2-0db01ead8d43)

2. เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
var myObj = new MyClass();

System.Console.WriteLine($"Default integer      F1 = {myObj.F1}");  //Implicit fields initialization
System.Console.WriteLine($"Default string       F2 = {myObj.F2}");
System.Console.WriteLine($"Initialized integer  F3 = {myObj.F3}");  //Explicit field initialization
System.Console.WriteLine($"Initialized string   F4 = {myObj.F4}");

class MyClass
{
    public int F1;
    public string F2;
    public int F3 = 100;
    public string F4 = "ASDF";
}
```
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-05/assets/144197034/e581aca1-b005-482c-91ca-7d728b295b86)

3. Build project โดยการใช้คำสั่ง

```
dotnet build  Lab05_Ex04
```

4. บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-05/assets/144197034/599f2661-e82d-4cf0-9c19-066c865f37d5)
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-05/assets/144197034/fe8a26ce-58f4-4630-a494-4cec163a5ddc)


6. Run project โดยการใช้คำสั่ง

```
dotnet run --project Lab05_Ex04
```

6. บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![ภาพ](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-05/assets/144197034/39762aab-e0b4-4079-807e-fecd4b942692)


7. อธิบายสิ่งที่พบในการทดลอง

จากการทดลองนี้เป็นการสร้างอ็อบเจกต์ของคลาส MyClass และพิมพ์ค่าของฟิลด์ทั้งหมดในอ็อบเจกต์นั้นออกทางคอนโซล

ในคลาส MyClass เรามีฟิลด์ 4 ฟิลด์คือ F1, F2, F3, และ F4 ซึ่งมีการกำหนดค่าต่างกันดังนี้:

F1 และ F2 ไม่ได้กำหนดค่าเริ่มต้น (implicit fields initialization)

F3 กำหนดค่าเริ่มต้นให้เป็น 100 (explicit field initialization)

F4 กำหนดค่าเริ่มต้นให้เป็น "ASDF" (explicit field initialization)

ผลลัพธ์ที่แสดงในคอนโซลจะแสดงค่าของฟิลด์ที่เราได้กำหนด โดยค่าของ F1 และ F2 จะเป็นค่าเริ่มต้นของชนิดข้อมูลนั้นๆ ซึ่งในกรณีของ int จะเป็น 0 และในกรณีของ string จะเป็น null ในขณะที่ F3 และ F4 จะแสดงค่าที่เรากำหนดไว้
ผลลัพธ์ที่ได้ 

Default integer      F1 = 0

Default string       F2 = 

Initialized integer  F3 = 100

Initialized string   F4 = ASDF


โดย F1 และ F2 จะแสดงค่าเริ่มต้นสำหรับชนิดข้อมูลนั้น ๆ ซึ่งคือ 0 สำหรับ int และ null สำหรับ string และ F3 และ F4 จะแสดงค่าที่เรากำหนดไว้ในการกำหนดค่าเริ่มต้น expliciltly

ในการทดลองนี้ เราสร้างอ็อบเจกต์ของคลาส MyClass และกำหนดค่าให้กับฟิลด์ทั้งสี่ฟิลด์ที่มีในคลาสนั้น จากนั้นเราแสดงผลลัพธ์ของค่าของแต่ละฟิลด์ออกทางคอนโซล

ในคลาส MyClass มีฟิลด์ทั้งหมด 4 ฟิลด์ ได้แก่ F1, F2, F3, และ F4 โดย:

 F1 และ F2 ไม่ได้รับการกำหนดค่าเริ่มต้นในการประกาศ ซึ่งจะมีค่าเริ่มต้นเป็น 0 สำหรับ int และ null สำหรับ string
     
F3 ถูกกำหนดค่าให้เป็น 100 ในการประกาศ
   
 F4 ถูกกำหนดค่าให้เป็น "ASDF" ในการประกาศ
   
ฟิลด์ F1 และ F2 ไม่ได้รับการกำหนดค่าจึงมีค่าเริ่มต้นเป็น 0 สำหรับ F1 และ null สำหรับ F2
   
ฟิลด์ F3 และ F4 ได้รับการกำหนดค่าเริ่มต้นอย่างชัดเจนในการประกาศ ซึ่งมีค่าตามที่กำหนดไว้
