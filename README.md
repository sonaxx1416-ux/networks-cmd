<p align="center">
  <img src="Gemini_Generated_Image_gpkfsigpkfsigpkf.png" width="300" alt="networks-cmd logo">
</p>

---

# 🌐 networks-cmd
[![Language](https://img.shields.io/badge/Language-English%20%2F%20Arabic-blue.svg)]()
[![Python](https://img.shields.io/badge/Python-3.x-green.svg)]()

---

### 🇸🇦 الوصف (العربية)
مكتبة `networks-cmd` هي أداة برمجية مبسطة للتحكم في شبكات الواي فاي على نظام ويندوز. بدلاً من التعقيد في أوامر `subprocess` والتعامل مع نصوص الـ `netsh` الطويلة، توفر لك هذه المكتبة دوال مباشرة وسهلة لأتمتة كل ما يخص الشبكات.

### 🇺🇸 Description (English)
The `networks-cmd` library is a simplified wrapper for Windows Wi-Fi management. Instead of dealing with complex `subprocess` commands and messy `netsh` parsing, this library provides a clean, professional API to handle network automation with ease.

---

### 🛠️ المميزات | Features
*   🚀 **سريعة | Fast**
*   🛡️ **سهلة | Easy** 
*   🤖 **أتمتة | Automation**

---

### 🧠 متطلبات المكتبة | Library requirements

* 💻 **نظام ويندوز | Windows System** 
##### وبعض الأحيان تحتاج لي صلاحيات مسؤول | And sometimes you need administrator privileges

---

### 📖 مرجع الدوال | API Reference

| Function | الوصف (العربية) | Description (English) |
| :--- | :--- | :--- |
| `networks_cmd.get_current_wifi()` | الحصول على اسم الشبكة الحالية | Get current network name |
| `networks_cmd.get_password(wifi_name)` | سحب كلمة السر للشبكة | Get saved password |
| `networks_cmd.connect_wifi(wifi_name, password)` | الاتصال بشبكة جديدة | Connect to a new Wi-Fi |
| `networks_cmd.disconnect()` | قطع الاتصال | Disconnect current Wi-Fi |
| `networks_cmd.delete_wifi(wifi_name)` | حذف بروفايل الشبكة | Delete a network profile |
| `networks_cmd.get_available()` | عرض الشبكات المتاحة | Show available networks |
| `networks_cmd.get_ping(target)` | فحص سرعة الاستجابة | Check ping to a target |
| `networks_cmd.get_connect()` | `True` = لاسلكي , `False` = سلكي | `True` = Wired , `False` =  Wireless or otherwise |
| `networks_cmd.clear_any_wifi()` | حذف بروفايل كل الشبكات | clear profiles wifi | 
| `networks_cmd.get_ip_humans()` | سحب `ip` كل الذي معك لي الشبكة | It pulls the `ip` of everyone who is with you on the network |
| `networks_cmd.get_ip_website(website_link)` | يسحب `ip` الموقع الذي تختاره | It pulls the `ip` of the location you choose | 

---

### 📚 المكتبات المستعلمة | Used libraries
| Library | (العربية) الوصف | Description (English) |
| :--- | :--- | :---
| `os` | للتحكم في النظام | To control the system | 
| `subprocess` | لي تنفيذ الأوامر | To execute the orders | 
| `re` | هي الأداة المسؤولة عن معالجة النصوص في هذا المشروع؛ نستخدمها لاستخراج البيانات بدقة من مخرجات الـ `cmd` وتحويلها إلى قيم برمجية منظمة. | It is the tool responsible for processing text in this project; we use it to extract data accurately from `cmd` outputs and convert it into organized programming values. | 

---

### 🆚 التحديث الحالي | Current update 
| : `0.2.0` : |

---

### 👾 طريقة التحميل | Download method
```consol
pip install networks-cmd
```
---

### 💡 مثال سريع | Quick Example

#### الحصول على الشبكة الحالية و كلمة المرور الخاصة بها | Obtain the current network and its password
```python
import networks_cmd as nc

wifi = nc.get_current_wifi()

password = nc.get_password(wifi)

print(f"[*] Network: {wifi} | Password: {password}")
```
### الحصول على البنيغ الحالي | Getting the current ping
```python
import networks_cmd as nc

ping = nc.get_ping()

print(f'ping : {ping}mc')
```
#### قطع الإتصال عن الشبكة الحالية | Disconnect from the current network
```python
import networks_cmd as nc

nc.disconnect()
```
#### الإتصال بي شبكة معينة  | Connecting to a specific network
```python
import networks_cmd as nc

nc.connect_wifi('WIFI_NAME', 'MY PASSWORD123')
```
