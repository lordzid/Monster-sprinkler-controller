# Monster sprinkler controller
<div align="center">
  <img src="https://esphome.io/_images/sprinkler.png" alt="Monster Sprinkler">
</div>


# Sprinkler Controller "Monster"  
**by ZID**

## Monster: Your Autonomous Smart Irrigation Assistant  
*Monster* is a smart **ESP32-based** device designed to manage irrigation with maximum autonomy and ease. It’s perfect for those who want their garden, lawn, or shrubs to stay well-maintained without constant attention, even without internet access. Featuring local control via buttons and an LCD display, built-in real-time clock, and additional options through a web server and Home Assistant integration, *Monster* blends reliability with modern technology.

Imagine you have a countryside home with a small garden, a neat lawn, shrubs along the fence, and decorative **"Golden Smaragd"** thuja trees by the entrance. You love keeping everything pristine but don’t want to spend time watering daily or worry about plants drying out while you’re away. That’s where *Monster* steps in — your autonomous helper.

### How It Works  

#### On-Site Setup  
You install *Monster* near your irrigation system and connect the valves for four zones: **"Golden Smaragd"** (2 valves for the thuja), **"Lawn"** (3 valves for the lawn), **"Garden"** (1 valve for the garden), and **"Bushes"** (2 valves for the shrubs). No internet is needed — all control is local.  
Using the **"Button UP"**, **"Button DOWN"**, and **"Menu Button"**, you access the LCD menu. First, set the time via **"Time setting"**: select the current year (**"Year set"**), month (**"Month set"**), day (**"Day set"**), hours (**"Hour set"**), and minutes (**"Minutes set"**), then save with **"Set Manual Time"**. The clock now runs independently, no network required.

#### Creating Schedules  
Suppose the thuja need watering three times a week, the lawn twice, the garden once, and the shrubs every other day. You enter **"Smaragd Schedule"** and configure:  
- **"Schedule 1"** — watering at `07:00` on Mondays, Wednesdays, and Fridays (**"Smaragd Monday"**, **"Smaragd Wednesday"**, **"Smaragd Friday"**), 15 minutes (**"1 Duration"**).  
- For the lawn in **"Lawn Schedule"**, set **"Schedule 1"** — `06:30` on Tuesdays and Saturdays (**"Lawn Tuesday"**, **"Lawn Saturday"**), 20 minutes (**"2 Duration"**).  
- The garden (**"Garden Schedule"**) waters on Thursdays at `08:00` (**"Garden Thursday"**), 10 minutes (**"Duration"**).  
- Shrubs (**"Bushes Schedule"**) — every other day at `19:00`, 12 minutes (**"1 Duration"**).  
Each step is confirmed with a sound (if **"Sound ON/OFF"** is enabled), and the display backlight (**"Auto Bright"**) activates for easy evening use.

#### Autonomous Operation  
You head to the city for a week. *Monster* follows the schedule: Monday morning waters the thuja, Tuesday the lawn, Thursday the garden, and so on. If it rains, you’ve pre-activated **"24h Rain Delay"** with a long button press — irrigation pauses for a day. The RGB LED glows **blue** on startup, then **red**, indicating Wi-Fi is off (you don’t need it).

#### Web Server Check  
Back home, you connect *Monster* to Wi-Fi via **"WiFi ON/OFF"**. On your phone, you open the web interface using **"IP Address"** and see: **"Smaragd Days Status"** lists completed days, **"Sprinkler Remaining Time Lawn"** shows the lawn watering (5 minutes left), and **"RAM Usage"** and **"Uptime"** confirm stable performance. You can even manually trigger **"Garden Active"** to refresh the garden after a hot day.

#### Home Assistant Control  
For added comfort, you link *Monster* to *Home Assistant*. Your smartphone now shows: **"Smaragd Schedule 1 Time"** (`07:00–07:15`), **"Lawn Valve 2 Status"** (on), **"Sprinkler Remaining Time Bushes"** (⏳ `0:08`). You can turn off shrub watering if the soil’s already damp, all from your couch.

### Why You Need It  
- **Time-Saving**: *Monster* handles irrigation while you relax or work.  
- **Flexibility**: Tailor schedules to your plants — from rare garden watering to frequent lawn care.  
- **Reliability**: It runs on your settings even without internet or power (with a backup).  
- **Convenience**: Choose local menus, web server, or *Home Assistant* for control.

---

## Core Features  

1. **Fully Autonomous Irrigation Control**  
*Monster* manages four zones — **"Golden Smaragd"**, **"Lawn"**, **"Garden"**, and **"Bushes"** — without needing a network. Set up to three schedules per zone:  
   - *Start Time*: Pick hours and minutes.  
   - *Days of the Week*: Choose days (e.g., **"Smaragd Monday"** or **"Lawn Sunday"**).  
   - *Duration*: Set valve run times (e.g., **"Smaragd 1 Run Duration"**, **"Garden Duration"**).  
   - *Repeats*: Define cycles (**"Smaragd Repeat Count"**, **"Lawn Repeat Count"**).  
It auto-starts irrigation, switches valves (e.g., **"Smaragd 1 Active"**, **"Lawn 2 Active"**), and supports sequential zoning (**"Smaragd Auto Advance"**), running flawlessly without Wi-Fi or servers.

2. **Local Display and Button Interface**  
Control is at your fingertips:  
   - **"Menu Button"**: Opens an intuitive LCD menu.  
   - **"Button UP"** and **"Button DOWN"**: Navigate settings or pages.  
   - Browse zones (**"Smaragd Schedule"**, **"Lawn Schedule"**), time (**"Time setting"**), or brightness (**"Brightness"**).  
The display shows the active zone, valve status (**"Smaragd Valve 1 Status"**), remaining time (**"Sprinkler Remaining Time Garden"**), and alerts like **"WiFi on!"** or **"Rain Delay"**.

3. **Internet-Free Real-Time Clock**  
*Monster*’s built-in clock runs independently. Set it manually in **"Time setting"**:  
   - **"Year set"** (year),  
   - **"Month set"** (month),  
   - **"Day set"** (day),  
   - **"Hour set"** (hours),  
   - **"Minutes set"** (minutes).  
Hit **"Set Manual Time"** to save, ensuring schedules work without external sync.

4. **Rain Delay Protection**  
Prevent overwatering with **"24h Rain Delay"** or **"48h Rain Delay"**. Activate via menu or long button press, pausing irrigation for 24 or 48 hours before resuming automatically.

5. **Audible Feedback**  
Actions come with sound (if **"Sound ON/OFF"** is on), making interaction lively and clear — think page switches or menu selections.

6. **RGB Status Indication**  
The RGB LED pulses to show status:  
   - **Blue**: Device booting.  
   - **Green**: Wi-Fi connected (**"WiFi is connected!"**).  
   - **Red**: Wi-Fi off or error.  
   - *Other hues*: Home Assistant link or valve activity.

7. **Display Backlight Control**  
Adjust **"Brightness"** manually (`0%–100%`) or enable **"Auto Bright"** for 10-second illumination on button press, saving power and enhancing usability anytime.

---

## Menu Functions  
*Monster*’s menu, accessed via **"Menu Button"**, is the core of local control, organized into handy groups:  

### Rain Delay Control  
- **"24h Rain Delay"**: Toggle a 24-hour irrigation pause for rainy days.  
- **"48h Rain Delay"**: Set a 48-hour delay.

### Irrigation Schedule Setup  
- **"Smaragd Schedule"** (*"Golden Smaragd"*):  
  - **"Schedule 1"**, **"Schedule 2"**, **"Schedule 3"**: Enable/disable and set times (**"Smaragd Schedule 1 Time"**).  
  - **"Select days"**: Pick days (**"Smaragd Monday"** to **"Smaragd Sunday"**).  
  - **"1 Duration"**, **"2 Duration"**: Set valve run times.  
  - **"Repeat Count"**: Number of cycles.  
  - **"Zone 1 Auto"**, **"Zone 2 Auto"**: Auto valve mode.  
  - **"Smaragd AA"**: Sequential valve switching.  
  - **"Smaragd Cycl"**: Full cycle activation.  

- **"Lawn Schedule"** (*"Lawn"*):  
  - **"Schedule 1"**, **"Schedule 2"**, **"Schedule 3"**: Times (**"Lawn Schedule 1 Time"**).  
  - **"Select days"**: Days (**"Lawn Monday"** to **"Lawn Sunday"**).  
  - **"1 Duration"**, **"2 Duration"**, **"3 Duration"**: Valve durations.  
  - **"Repeat Count"**: Cycles.  
  - **"Zone 1 Auto"**, **"Zone 2 Auto"**, **"Zone 3 Auto"**: Auto mode.  
  - **"Lawn AA"**: Sequential switching.  
  - **"Lawn Cycl"**: Full cycle.  

- **"Garden Schedule"** (*"Garden"*):  
  - **"Schedule 1"**, **"Schedule 2"**, **"Schedule 3"**: Times (**"Garden Schedule 1 Time"**).  
  - **"Select days"**: Days (**"Garden Monday"** to **"Garden Sunday"**).  
  - **"Duration"**: Valve run time.  

- **"Bushes Schedule"** (*"Bushes"*):  
  - **"Schedule 1"**, **"Schedule 2"**, **"Schedule 3"**: Times (**"Bushes Schedule 1 Time"**).  
  - **"Select days"**: Days (**"Bushes Monday"** to **"Bushes Sunday"**).  
  - **"1 Duration"**, **"2 Duration"**: Valve durations.  
  - **"Repeat Count"**: Cycles.  
  - **"Zone 1 Auto"**, **"Zone 2 Auto"**: Auto mode.  
  - **"Bushes AA"**: Sequential switching.  
  - **"Bushes Cycl"**: Full cycle.  

### Display and Device Settings  
- **"Display Settings"**:  
  - **"Time setting"**: Submenu for time setup:  
    - **"Year set"**: Year.  
    - **"Month set"**: Month.  
    - **"Day set"**: Day.  
    - **"Hour set"**: Hours.  
    - **"Minutes set"**: Minutes.  
    - **"Set Time"**: Save time.  
  - **"Brightness"**: Adjust display brightness (`0–100%`).  
  - **"Auto Bright"**: Auto-backlight on button press.  
  - **"Sound"**: Toggle sounds on/off.  
  - **"WIFI auto"**: Auto Wi-Fi connection.  
  - **"WiFi ON/OFF"**: Manual Wi-Fi control.  
  - **"IP: [IP Address]"**: Current IP display.  
  - **"SSID: [Connected SSID]"**: Connected network name.  
  - **"WiFi Signal: [WiFi Signal]"**: Signal strength.  
  - **"Restart ESP"**: Reboot device.  
Each setting comes with a beep (if **"Sound"** is on) and backlight for nighttime ease.

---

## Web Server Features  
Connect *Monster* to Wi-Fi (**"WiFi ON/OFF"** or **"WIFI auto"**) for a local web interface:  
- View zone status (**"Smaragd Days Status"**, **"Lawn Schedule 1 Time"**).  
- Manually control valves (**"Smaragd 1 Active"**, **"Garden Active"**).  
- Track remaining time (**"Sprinkler Remaining Time Lawn"**).  
- Check device stats: **"IP Address"**, **"Connected SSID"**, **"WiFi Signal"**, **"RAM Usage"**, **"Flash Usage"**, **"Uptime"**.  
- Reboot via **"Restart"**.  
It’s local and internet-free, preserving autonomy.

---

## Home Assistant Integration  
For enhanced control, *Monster* integrates with *Home Assistant*, offering **"HA info"** data for all zones (**"Golden Smaragd"**, **"Bushes"**, **"Lawn"**, **"Garden"**):  
- **"Smaragd Days Status"**: Days selected (e.g., `"Mon Wed Fri"`).  
- **"Smaragd Schedule 1 Time"**: Start/end of first schedule (e.g., `"08:00 - 08:30"` or `"OFF"`).  
- **"Smaragd Schedule 2 Time"**: Second schedule time.  
- **"Smaragd Schedule 3 Time"**: Third schedule time.  
- **"Sprinkler Remaining Time (Golden Smaragd)"**: Active valve time (`⏳ "0:15"` or `❌ "No time zone running"`).  
- **"Smaragd Valve 1 Status"**: First valve state (on/off).  
- **"Smaragd Valve 2 Status"**: Second valve state.  
This lets you monitor and manage remotely, though local clocks and autonomy remain the priority.


---

## Why Monster is Perfect  
*Monster* is built for independence lovers. It runs locally on your settings and clock, with a web server for monitoring and *Home Assistant*’s **"HA info"** for smart home fans. Flexible yet simple, it keeps your lawn to garden thriving effortlessly.  
With *Monster*, your garden flourishes while you relax. **Autonomy**, **style**, and **smart tech** — all in one!

---
## Components

DS1307
<div align="center">
  <img src="./images/DS1307.jpg" alt="My Monster Sprinkler">
</div>

---

LCD PCF8574
<div align="center">
  <img src="./images/lcd.jpg" alt="My Monster Sprinkler">
</div>

---

XL9535
<div align="center">
  <img src="./images/XL9535.png" alt="My Monster Sprinkler">
</div>

---

Rtttl Buzzer
<div align="center">
  <img src="./images/buzzer.jpg" alt="My Monster Sprinkler">
</div>

---

Button
<div align="center">
  <img src="./images/membrane-switch-1x3.jpg" alt="My Monster Sprinkler">
</div>

---

<div align="center">
  <h3><b>Web Server</b></h3>
</div>

---

<div align="center">
  <img src="./images/web server.jpg" alt="My Monster Sprinkler">
</div>

---

Learn more from *Home Assistant* community members **[GrahamS](https://community.home-assistant.io/u/grahams/summary)** and **[raythefourth](https://community.home-assistant.io/u/raythefourth/summary)**, who contribute to such integrations.


