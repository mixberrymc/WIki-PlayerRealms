---
icon: square-sliders
---

# settings.yml

settings.yml เป็นไฟล์ตั้งค่าสำหรับปลั๊กอิน

### Database (ฐานข้อมูล)

```
database:
  host: '127.0.0.1'
  port: 3306
  user: 'root'
  password: '' // ควรเปลี่ยนรหัสผ่านเริ่มต้น
  database: 'realms'
```



### Worlds

```
lobby-world: 'world'
plot-world: 'realms'
```

* **lobby-world**: ตั้งค่าโลกล็อบบี้ สำหรับการดึงผู้เล่นกลับมาในกรณีที่โลกหมดอายุ หรือเจ้าของ Realm ออฟไลน์
* **plot-world**: ตั้งค่าโลกเรียม (โลกจะไม่สร้างอัติโนมัติ ผู้ดูแลต้องสร้างโลกเองโดยใช้ปลั๊กอินอื่น เช่น Multiverse-Core)



### Default Realm Setting (ตั้งค่าเริ่มต้น)

กำหนดการตั้งค่าของ Realm เริ่มต้น

```
default-realm-setting:
  maxOnline: 3
  borderSize: 400
```

* **maxOnline**: จำนวนผู้เล่นสูงสุดใน Realm เริ่มต้น
* **borderSize**: ขนาด World Border เริ่มต้น

{% hint style="warning" %}
ห้ามตั้ง borderSize สูงกว่า realm-distance
{% endhint %}



### Realm Distance

กำหนดระยะห่างระหว่าง Realm

{% hint style="danger" %}
ไม่ควรเปลี่ยน realm distance หลังจากเปิดและให้บริการเซิร์ฟเวอร์แล้ว เนื่องจากอาจทำให้ Realms ของผู้เล่นซ้อนทับกันได้ และอาณาเขตของ Realms จะไม่เปลี่ยนตาม
{% endhint %}

```
realm-distance: 800
```
