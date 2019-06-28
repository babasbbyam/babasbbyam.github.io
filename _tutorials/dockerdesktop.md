---
title: Docker Desktop 
layout: tutorial
---

download [ Docker for Windows ](https://hub.docker.com/editions/community/docker-ce-desktop-windows)

- สำหรับ Window 10 Pro หรือ Education ขึ้นไป และมี account docker hub
- ใช้ Hyper-V เป็น VM engine แต่จะทำให้ VirtualBox ทำงานไม่ได้

![docker-enable-hyper-v](/assets/docker-enable-hyper-v.png)

รูปที่ 1 ใช้งาน docker ในโหมดของ Hyper-V แต่จะทำให้ VirtualBox ทำงานไม่ได้ หลังจากนั้นเครื่องจะ Restart และ Docker จะถูกใช้งาน อัตโนมัติ

เมื่อกด OK จะเปิดใช้งาน Feature Hyper-V อัตโนมัติ แต่หากไม่สำเร็จ ศึกษาวิธีการเปิด Feature Hyper-V ได้ที่ [ลิ้งนี้](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v)

![dockerdesktop](/assets/dockerdesktop.png)

รูปที่ 2 หน้าต่างล็อกอินเข้าสู่ Docker ซึ่งผู้ใช้งานจะต้องทำการสมัครสมาชิกก่อนถึงจะสามารถใช้งานได้

ตั้งค่า Shared Drive คลิกขวาที่ไอคอน Docker ที่ Task bar เลือก Settings ไปที่ Shared Drive เลือก drive ที่ต้องแชร์ แล้วกด Apply

![diveCD](/assets/diveCD.png)

รูปที่ 3 การตั้งค่า Shared Drive

ซึ่งเมื่อเปิดใช้งาน Hyper-V แล้วจะทำให้ไม่สามารถใช้งาน Virtualbox หรือ Virtualization Software อื่นได้ ซึ่งหากต้องการใช้ VM สามารถใช้งาน Hyper-V ทดแทนได้ โดยใช้งานผ่าน Hyper-V Manager

![HyperV](/assets/HyperV.png)

รูปที่ 4 หน้าต่างของ Hyper-V Manager

การตรวจสอบความสำgit เร็จหลังการติดตั้งซอฟแวร์ต่างๆผ่าน Windows PowerShell
ตรวจสอบ การติดตั้งโปรแกรมแต่ละอันผ่าน command line / PowerShell โดยใช้คำสั่งดังนี้

```
git --version
python --version
pip --version
docker --version
```

![powershell-check](/assets/powershell-check.png)

รูปที่ 5 คำสั่งและการแสดงผลของเวอร์ชันของซอฟแวร์แต่ละรุ่น
