# ARCH-02 · แผนภาพสถาปัตยกรรม

> คัดลอกไฟล์นี้ไปเป็น `docs/arch-02-diagrams/README.md` แล้ววางไฟล์แผนภาพไว้ในโฟลเดอร์เดียวกัน
> รุ่นแรก T05–T06 (D04) · Deployment T08 (D06) · ตรวจใน A5a (T07) และ A5b (T14) · CLO3
> ทุกภาพต้องมี **ไฟล์ต้นฉบับที่แก้ได้** (`.drawio`) คู่กับ **ภาพ** (`.png` หรือ `.svg`) ชื่อเดียวกัน

## รายการแผนภาพ

| แผนภาพ | ไฟล์ต้นฉบับ | ภาพ | เริ่ม / ปรับล่าสุด | ตรงกับระบบรุ่น (tag / commit) |
|---|---|---|---|---|
| C4 Context | `c4-context.drawio` | `c4-context.png` | T05 | |
| C4 Container | `c4-container.drawio` | `c4-container.png` | T05 → T07 | |
| Deployment (local + Cloud) | `deployment.drawio` | `deployment.png` | T08 → T14 | |
| Dynamic / Sequence ของหนึ่ง flow | `sequence-<ชื่อ flow>.drawio` | `sequence-<ชื่อ flow>.png` | T12 → T14 | |
| C4 Component (ถ้าจำเป็น) | `c4-component-<ชื่อ>.drawio` | | | |

## C4 Context

![C4 Context](c4-context.png)

คำอธิบายสั้น: ผู้ใช้กลุ่มใด ใช้ระบบทำอะไร และระบบเชื่อมกับระบบภายนอกใด

## C4 Container

![C4 Container](c4-container.png)

| Container | เทคโนโลยี | หน้าที่ | สื่อสารกับ (protocol / port) |
|---|---|---|---|
| | | | |

> C4 Container คือหน่วยซอฟต์แวร์ที่รันแยกกัน ไม่จำเป็นต้องตรงกับ Docker container หนึ่งตัว

## Deployment

![Deployment](deployment.png)

| สภาพแวดล้อม | ที่รัน | ตัวแปร / secrets ที่ต้องตั้ง | ข้อมูลที่ต้องคงอยู่ |
|---|---|---|---|
| local | Docker Compose | | |
| Cloud | Railway | | |

## Sequence ของ flow: <ชื่อ flow>

![Sequence](sequence-flow.png)

กรณีผิดพลาดที่แสดงในภาพ:

## ความสอดคล้องกับระบบ

- ภาพทุกภาพตรงกับโค้ดและ `docker-compose.yml` รุ่นใด:
- สิ่งที่ภาพละไว้โดยตั้งใจ:

## ประวัติการแก้ไข

| วันที่ | ภาพ | แก้อะไร | เพราะอะไร |
|---|---|---|---|
| | | | |
