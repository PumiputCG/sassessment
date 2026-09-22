# SAssessment

## SAssessment คืออะไร / About

ระบบประเมินผลพนักงานประจำปีที่คิดคะแนนตามน้ำหนักของแต่ละหมวด เช่น Attendance, Individual Performance, Department OKR และ Company OKR แล้วรวมออกมาเป็นคะแนนสุดท้ายพร้อมเกรด ผลงานนี้ได้รับรางวัลชนะเลิศจากกิจกรรม Kaizen ภายในองค์กร

An annual performance review system that scores each employee by weighted categories such as Attendance, Individual Performance, Department OKR and Company OKR, then turns them into a final score and grade. It won first place in the company's internal Kaizen competition.

## ทำอะไรได้บ้าง / Features

- เปิดรอบประเมิน และปิดรอบเป็นแบบอ่านอย่างเดียวเมื่อจบ เพื่อไม่ให้แก้ผลย้อนหลัง
- นำเข้ารายชื่อพนักงานจาก Excel โดยมี template ให้ดาวน์โหลด
- พนักงานประเมินตัวเองก่อน แล้วหัวหน้าจึงให้คะแนน
- คำนวณคะแนนตามน้ำหนักแต่ละหมวด รวมโบนัสและการหักคะแนน แล้วออกมาเป็นเกรด
- สรุปผลและส่งออกเป็น Excel พร้อมประวัติย้อนหลังของแต่ละคน
- ลืมรหัสผ่านก็รีเซ็ตเองได้

* Open review cycles and lock finished ones as read-only so results cannot be changed later
* Import employees from Excel with a downloadable template
* Employees assess themselves first, then managers score them
* Weighted scoring across categories, including bonuses and deductions, turned into a grade
* Summaries and Excel exports with each person's history
* Self-service password reset

## Tech Stack

**Backend:** PHP 8, Laravel 12, Laravel Excel

**Frontend:** Blade, Tailwind CSS, Bootstrap 5, Bootstrap Icons, AOS, Vite

**Database:** MySQL

## ติดตั้ง / Installation

ต้องมี PHP 8.2 ขึ้นไป, Composer, Node.js และ MySQL ก่อนรัน migrate ให้แก้ค่า `DB_*` ใน `.env` ให้ตรงกับฐานข้อมูลในเครื่อง

Requires PHP 8.2+, Composer, Node.js and MySQL. Set the `DB_*` values in `.env` before migrating.

```bash
git clone https://github.com/PumiputCG/sassessment.git
cd sassessment
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan migrate
npm run build
php artisan serve
```
