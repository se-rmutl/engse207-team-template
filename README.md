# ENGSE207 · S?-T?? · ชื่อทีม

> repo ของทีมสำหรับ Term Project รายวิชา **ENGSE207 สถาปัตยกรรมซอฟต์แวร์** ภาคการศึกษาที่ 2/2569
> แก้บรรทัดหัวเรื่องเป็นรหัสทีมและชื่อทีมของคุณ เช่น `# ENGSE207 · S1-T03 · ทีมเมฆ`

| | |
|---|---|
| สมาชิก บทบาท และกติกาทีม | [docs/team-charter.md](docs/team-charter.md) |
| Cloud URL (ตั้งแต่ T08) | _ยังไม่มี_ |
| กำหนดส่งของ SEC | <https://se-rmutl.github.io/engse207/deliverables.html> |
| สถานะการส่งของทีม | <https://se-rmutl.github.io/engse207/submissions.html> |

---

## เริ่มต้น (ทำครั้งเดียว ก่อน T02)

1. **ตั้งชื่อ repo** `engse207-2569-s<SEC>-t<เลขทีม>` เช่น `engse207-2569-s1-t03` เลือก **Private**
2. **เพิ่มผู้มีสิทธิ์** Settings > Collaborators > Add people เพิ่ม `tkeatkaew` และเพื่อนในทีมทุกคน (เพื่อนต้องกดรับคำเชิญในอีเมล)
3. **ใส่ลิงก์ repo** ในแบบลงทะเบียนทีม (กดลิงก์ "แก้ไขคำตอบ")
4. **Team charter** คัดลอก [`templates/team-charter.md`](templates/team-charter.md) ไปเป็น `docs/team-charter.md` แล้วเติมให้ครบ
5. **ผลแล็บ T01** ทุกคนคัดลอก [`templates/T01-result.md`](templates/T01-result.md) ไปเป็น `individual/T01-<รหัสนักศึกษา>.md` ของตัวเอง
6. แก้หัวเรื่องของ README นี้ แล้ว commit และ push ทั้งหมดเข้า `main`

ภายใน 1 ชั่วโมง หน้าสถานะการส่งจะขึ้นว่าเปิด repo ได้ ถ้าไม่ขึ้น ตรวจว่าเพิ่ม `tkeatkaew` แล้ว และลิงก์ในแบบลงทะเบียนตรงกับ repo นี้ หรือกด "ตรวจทีมนี้ใหม่" ในหน้าสถานะการส่ง

## รันระบบ Task Board (ARCH-04)

> ส่วนนี้ทีมเขียนเองเมื่อได้ระบบตั้งต้นใน T02 และต้องเริ่มใหม่จากศูนย์ตามขั้นตอนนี้ได้ (clean start) ซึ่งเป็นส่วนหนึ่งของ A6

```bash
cp .env.example .env        # แล้วแก้ค่าใน .env (ไฟล์นี้ไม่ถูก commit)
docker compose up -d --build
docker compose ps
```

| บริการ | URL / port | หมายเหตุ |
|---|---|---|
| frontend | | |
| backend | | |
| database | | |

ล้างทั้งหมดเพื่อทดสอบ clean start: `docker compose down -v`

## ส่งงานอย่างไร

ส่งโดย **push ไฟล์ตาม path ด้านล่างเข้า branch `main`** ระบบตรวจทุกชั่วโมงว่ามีไฟล์ครบหรือยัง แล้วเทียบเวลา commit แรกของไฟล์กับกำหนดส่ง ระบบไม่ได้ตรวจเนื้อหา อาจารย์ตรวจและให้คะแนนแยก

- ชื่อไฟล์และโฟลเดอร์ต้องตรงทุกตัวอักษร ไฟล์ที่อยู่ใน branch อื่นยังไม่นับจนกว่าจะ merge
- แม่แบบอยู่ใน [`templates/`](templates/) **คัดลอก**ไปไว้ตาม path แล้วแก้ ไม่ต้องแก้ในโฟลเดอร์ templates
- จุดตรวจที่ใช้ tag ต้อง push tag ขึ้น GitHub ด้วย `git tag t07-a5a && git push origin t07-a5a`

```text
<repo>/
├── README.md                      วิธีรันแบบ clean start และ Cloud URL           D06 · A6
├── .env.example                   ตัวแปรที่ต้องตั้ง ไม่มีค่าจริง                     A6
├── docker-compose.yml             รันระบบทั้งชุดบนเครื่อง                           A6
├── frontend/  backend/            ระบบ Task Board ของทีม (ARCH-04)
├── docs/
│   ├── team-charter.md            สมาชิก บทบาท กติกาทีม                           D02
│   ├── arch-01-context.md         ARCH-01 บริบท ขอบเขต quality scenarios          D03 · A5a
│   ├── arch-02-diagrams/          ARCH-02 ไฟล์ .drawio ต้นฉบับ และภาพ .png/.svg    D04 · D06 · A5a · A5b
│   ├── arch-03-adr/               ADR-001-<ชื่อเรื่อง>.md · ADR-002-<ชื่อเรื่อง>.md · data-note.md
│   ├── arch-05-evaluation.md      ARCH-05 การประเมินจากหลักฐาน                    D09 · A7
│   ├── arch-06-handover.md        ARCH-06 บทสรุปส่งต่อ ไทย/อังกฤษ                  H06
│   ├── labs/t02.md … t14.md       บันทึกแล็บ ครั้งละไฟล์                            L02–L14
│   └── presentation/slides.pdf    สไลด์นำเสนอ T15                                 A8
└── individual/                    งานเดี่ยว ชื่อไฟล์ลงท้ายด้วยรหัสนักศึกษา
    ├── T01-<รหัส>.md              ผลแล็บ Docker T01                               I01
    ├── A1a-<รหัส>.md · A1b-<รหัส>.md   log และ diff ของจุดตรวจรายคน             A1
    ├── A2a-<รหัส>.md · A2b-<รหัส>.md   เหตุผลเลือกแบบ · อ่านผลทดลอง            A2
    ├── A9-log-<รหัส>.md           บันทึกบทบาท แหล่งอ้างอิง การใช้ AI ทุกครั้งสอน    A9
    └── A9-reflection-<รหัส>.md    Reflection ท้ายภาค                               A9
```

รหัสนักศึกษาเขียนเต็มแบบมีขีด เช่น `individual/T01-68543210000-0.md`

| แม่แบบ | คัดลอกไปเป็น |
|---|---|
| [team-charter.md](templates/team-charter.md) | `docs/team-charter.md` |
| [T01-result.md](templates/T01-result.md) | `individual/T01-<รหัส>.md` |
| [lab-note.md](templates/lab-note.md) | `docs/labs/tNN.md` เช่น `docs/labs/t02.md` |
| [arch-01-context.md](templates/arch-01-context.md) | `docs/arch-01-context.md` |
| [arch-02-diagrams.md](templates/arch-02-diagrams.md) | `docs/arch-02-diagrams/README.md` (คู่กับไฟล์ .drawio และภาพ) |
| [adr.md](templates/adr.md) | `docs/arch-03-adr/ADR-001-<ชื่อเรื่อง>.md` · `ADR-002-…` |
| [data-note.md](templates/data-note.md) | `docs/arch-03-adr/data-note.md` |
| [arch-05-evaluation.md](templates/arch-05-evaluation.md) | `docs/arch-05-evaluation.md` |
| [arch-06-handover.md](templates/arch-06-handover.md) | `docs/arch-06-handover.md` |
| [A1-log.md](templates/A1-log.md) | `individual/A1a-<รหัส>.md` · `individual/A1b-<รหัส>.md` |
| [A2a-rationale.md](templates/A2a-rationale.md) | `individual/A2a-<รหัส>.md` |
| [A2b-reading.md](templates/A2b-reading.md) | `individual/A2b-<รหัส>.md` |
| [A9-log.md](templates/A9-log.md) | `individual/A9-log-<รหัส>.md` |
| [A9-reflection.md](templates/A9-reflection.md) | `individual/A9-reflection-<รหัส>.md` |

## กติกา Git ของทีม

- `main` ต้องรันได้เสมอ งานใหม่ทำใน branch แล้วเปิด Pull Request ให้เพื่อนอีกคนรีวิวก่อน merge
- งานแต่ละชิ้นผูกกับ issue และมีผู้รับผิดชอบ
- ห้าม commit `.env` หรือ secrets ใช้ `.env.example` แทน
- ไฟล์งานเดี่ยวใน `individual/` เจ้าของไฟล์เป็นคน commit เอง
- ใช้ AI ได้ในแล็บ งานทีม และ A9 โดยระบุว่าใช้ส่วนไหนและตรวจผลก่อนใช้ ไม่ใช้ใน A1 และการสอบ

---

ENGSE207 สถาปัตยกรรมซอฟต์แวร์ · ภาค 2/2569 · มทร.ล้านนา · เว็บรายวิชา <https://se-rmutl.github.io/engse207/>
