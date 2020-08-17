# 📏1. Design Patterns vs Anti-patterns*



---
# 🏊  4. Object Pool Pattern
คือ Creational patterns ช่วยในการออกแบบเมื่อจะสร้าง Object ชนิดเดียวกันจำนวนมากๆ 
โดยทั่วไป Object pool คือก็คือที่เก็บ Object เมื่อ Object ถูกนำออกไปใช้ Object นั้นจะไม่สามารถใช้ได้ใน pool จนกว่าจะนำกลับมา
ซึ่ง Object ใน Pool จะมีวงจรชีวิตดังนี้   
- Creation
- Validation
- Destroy
![Ex](https://media.geeksforgeeks.org/wp-content/uploads/uml-pool-design.jpg)
- Clicent : คลาสที่ต้องการใช้ object
- ObjectPool : คลาสที่เก็บ list ของ Object ที่มีอยู่ และพร้อมใช้งาน ซึ่ง Clicent จะสื่อสารกับคลาสนี้เพื่อเช็คว่าตอนนี้ใน Pool มี Object ที่ต้องใช้
- ReusablePool : คลาสที่มีความจำกัดในการสร้าง หรือมีความจำกัดในการพร้อมใช้ ดังนั้นจึงจะต้องจัดเอาไว้ใน object pool

### ✔️ ข้อดี
-มีการเพิ่มประสิทธิภาพ
- จัดการการเชื่อมต่อและจัดหาวิธีการใช้ซ้ำและแบ่งปัน
- รูปแบบนี้จะใช้เมื่ออัตราการเริ่มต้น instance ของคลาสสูง

---
# 🙀 5. Functional Programming 
เป็น paradigm หนึ่งสำหรับการเขียนโปรแกรม โดยพัฒนามาจาก Lambda calculus  ซึ่งหลายเราอาจจะคุ้นเคยกับ paradigm อื่นอย่างเช่น 
object-oriented programming
## “Pure Function” 
การเขียนโปรแกรมแบบ functional นั้น เน้นไปที่การใช้ Pure Function  
### `(1) รับ input  → (2) นำ input มา operate →  (3) return ผลลัพธ์ออกไป`

### 📍ตัวอย่าง
```
function add(x, y) {
   return x + y;
}

```
สิ่งสำคัญที่สุดของ Functional Programming นั้น คือการลด **"side effect"** ที่เกิดจาก function ที่เขียนขึ้นมา  
ดังนั้นจึงต้องหลีกเลี่ยงการใช้ **"Shared state"** และ **"Mutable Data"** เพื่อป้องกันการเปลี่ยนแปลงของข้อมูล จะได้ไม่เกิดปัญหาตามมา

### ✔️ ข้อดี ของ Function Programming
- มีชื่อเสียงในเรื่อง high-level abstractions เพราะมันซ่อนรายละเอียดของ Routine operations อย่างเรื่องของ Iterating ไว้ ทำให้ Code สั้นลง และมี Errors เล็กน้อยที่พอจะสามารถยอมรับได้
- เนื่องจากภาษาและ Structure ที่มีความยืดหยุ่น มันจึงช่วยให้ Functional Programming Developer เข้าใกล้ปัญหาได้มากขึ้น นอกจากนี้มันยังมี Tools ที่ทั้งใหม่และน่าสนใจสำหรับการแก้ปัญหาที่ซับซ้อน ซึ่ง OOP Developers มักจะละเลยไป
- ช่วยให้สามารถเขียน Code ได้อย่างถูกต้อง และรวดเร็ว อีกทั้งการ Test และ Debug ก็ทำได้สะดวกขึ้น

### ❌ ข้อเสีย ของ Function Programming
- ไม่มี Vocabulary ที่มีประสิทธิภาพสำหรับ Functional Languages โดย Purely Functional Vocabularies ทำงานช้ากว่า  Hash tables และมันก็สร้างปัญหาในบาง Applications ได้ สำหรับ Developer ส่วนใหญ่แล้ว ไม่ค่อยมีใครสังเกตเห็นข้อบกพร่องนี้
- ไม่เหมาะสำหรับ Algorithm ในงานเกี่ยวกับ Graph เนื่องจากมันทำงานได้ช้า




