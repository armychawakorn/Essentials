# Essentials

**คำสั่งพื้นฐาน:**

- **`/rm [steamid] [id] [distance]`:**  ลบวัตถุบนแผนที่ (Permission: `supernovea.essentials.remove`)
    - `steamid` (ไม่บังคับ): SteamID64 ของผู้เล่นที่เป็นเจ้าของวัตถุ (หากไม่ระบุ จะลบวัตถุทั้งหมด)
    - `id` (ไม่บังคับ): ID ของวัตถุ (หากไม่ระบุ จะลบวัตถุทั้งหมด)
    - `distance` (ไม่บังคับ): ระยะทางสูงสุดจากผู้เล่น (เป็นหน่วยในเกม)
    - **ตัวอย่าง:**
        - `/rm 76561198012345678` (ลบวัตถุของผู้เล่นที่มี SteamID นี้)
        - `/rm * 1234` (ลบวัตถุที่มี ID เป็น 1234)
        - `/rm * * 10` (ลบวัตถุภายในรัศมี 10 หน่วยจากผู้เล่น)
        - `/rm 76561198012345678 1234 5` (ลบวัตถุที่มี ID เป็น 1234 ของผู้เล่นที่มี SteamID นี้ภายในรัศมี 5 หน่วย)

- **`/rmwo [steamid]`:**  ลบวัตถุทั้งหมดบนแผนที่ ยกเว้นของผู้เล่นที่มี SteamID นี้ (Permission: `supernovea.essentials.removewithout`)
    - `steamid`: SteamID64 ของผู้เล่นที่ต้องการยกเว้น
    - **ตัวอย่าง:**
        - `/rmwo 76561198012345678` (ลบวัตถุของทุกคน ยกเว้นผู้เล่นนี้)

- **`/setwarp <warp_name>`:**  กำหนดตำแหน่งวาร์ปใหม่ (Permission: `supernovea.essentials.setwarp`)
    - `warp_name`: ชื่อของวาร์ป
    - **ตัวอย่าง:**
        - `/setwarp spawn` (กำหนดวาร์ปชื่อ "spawn")

- **`/warp <warp_name>`:**  วาร์ปไปยังตำแหน่งวาร์ป (Permission: `supernovea.essentials.warp.<warp_name>`)
    - `warp_name`: ชื่อของวาร์ป
    - **ตัวอย่าง:**
        - `/warp spawn` (วาร์ปไปยังวาร์ปชื่อ "spawn")

- **`/warps`:**  แสดงรายการวาร์ปที่มีอยู่ (Permission: `supernovea.essentials.warps`)
    - **ตัวอย่าง:**
        - `/warps` (แสดงรายการวาร์ปทั้งหมด)

- **`/delwarp <warp_name>` หรือ `/deletewarp <warp_name>`:**  ลบวาร์ป (Permission: `supernovea.essentials.delwarp`)
    - `warp_name`: ชื่อของวาร์ป
    - **ตัวอย่าง:**
        - `/delwarp spawn` (ลบวาร์ปชื่อ "spawn")

- **`/home`:**  วาร์ปกลับไปที่เตียงของผู้เล่น (Home) (Permission: `supernovea.essentials.home`)
    - **ตัวอย่าง:**
        - `/home` (วาร์ปไปที่เตียง)

- **`/speed <speed>`:**  ตั้งค่าความเร็วการเคลื่อนที่ของผู้เล่น (Permission: `supernovea.essentials.speed`)
    - `speed`: ค่าความเร็ว (ค่าเริ่มต้นคือ 1)
    - **ตัวอย่าง:**
        - `/speed 2` (เพิ่มความเร็วเป็น 2 เท่า)
- **`/gotomarker หรือ /gtm`:**  วาร์ปไปยังตำแหน่ง Marker  ของผู้เล่น  (Permission:  `supernovea.essentials.gotomarker`)
    -   **ตัวอย่าง:**
        -   `/gotomarker`  (วาร์ปไปยัง Marker)

**คำสั่งเพิ่มเติม:**

- **`/if <feature> <on|off>`:**  ควบคุมฟีเจอร์ของไอเทม (Permission: `supernovea.essentials.itemfeature`)
    - `feature`: ฟีเจอร์ที่ต้องการควบคุม (autoreload, autorepair, หรือ all)
    - `on/off`: เปิดหรือปิดฟีเจอร์
    - **ตัวอย่าง:**
        - `/if autoreload on` (เปิด autoreload)
        - `/if autorepair off` (ปิด autorepair)
        - `/if all on` (เปิดทั้ง autoreload และ autorepair)

- **`/vf <feature> <on|off>`:**  ควบคุมฟีเจอร์ของยานพาหนะ (Permission: `supernovea.essentials.vehiclefeature`)
    - `feature`: ฟีเจอร์ที่ต้องการควบคุม (autorefuel, autorepair, หรือ all)
    - `on/off`: เปิดหรือปิดฟีเจอร์
    - **ตัวอย่าง:**
        - `/vf autorefuel on` (เปิด autorefuel)
        - `/vf autorepair off` (ปิด autorepair)
        - `/vf all on` (เปิดทั้ง autorefuel และ autorepair)

- **`/ci [player name/steamid]`:** ล้าง Inventory ของผู้เล่น (Permission: `supernovea.essentials.clearinventory`)
    - `player name/steamid`: ชื่อหรือ SteamID ของผู้เล่น (หากไม่ระบุ จะล้าง Inventory ของตัวเอง)
    - **ตัวอย่าง:**
        - `/ci PlayerName` (ล้าง Inventory ของ PlayerName)
        - `/ci 76561198012345678` (ล้าง Inventory ของผู้เล่นที่มี SteamID นี้)
        - `/ci` (ล้าง Inventory ของตัวเอง)

**หมายเหตุ:**

-  อย่าลืมกำหนดสิทธิ์ให้กับผู้เล่นหรือยศในไฟล์ `Permissions.config.xml` เพื่อให้ผู้เล่นสามารถใช้คำสั่งเหล่านี้ได้
