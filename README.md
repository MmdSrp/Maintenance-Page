# Maintenance Website 🏗️

This repository contains a beautiful "Maintenance" website built with HTML, TailwindCSS, and JavaScript. It features a countdown timer, a newsletter subscription form, social media links, and a modern gradient design. The project includes two versions: one in Persian (Farsi) and one in English.

---

## فارسی (Persian)

### این پروژه چیه؟ 😎

این یه صفحه وب‌سایت خوشگل و ساده‌ست که می‌گه «سایت در حال تعمیر و نگهداریه»! با HTML، TailwindCSS و یه کم جاوااسکریپت درستش کردم. اگه می‌خوای به کاربرات بگی سایتت موقتاً در حال به‌روزرسانیه، این صفحه خیلی به کار میاد. چیزایی که توش داره ایناست:

- **تایمر شمارش معکوس** ⏳: نشون می‌ده چقدر مونده تا سایتت دوباره آماده بشه.
- **فرم اشتراک**: کاربرا می‌تونن ایمیلشون رو بذارن تا خبرای جدید بهشون برسه.
- **لینک شبکه‌های اجتماعی**: می‌تونی لینک اینستا، توییتر یا هر چی دوست داری بذاری.
- **دیزاین باحال**: یه گرادیان خوش‌رنگ با انیمیشنای نرم و شیک.
- **سازنده**: نوشته «توسعه یافته توسط MmdSrp» و یه لینک به پروژه‌های دیگم.

فایلای پروژه:

- `index-fa.html`: نسخه فارسی.
- `index-en.html`: نسخه انگلیسی.

### چطور زمان تایمر رو عوض کنم؟

تایمر این صفحه یه تاریخ مشخص داره که تو مرورگر (localStorage) ذخیره می‌شه. اگه بخوای زمانش رو عوض کنی، باید یه کم کد جاوااسکریپت رو دستکاری کنی. نگران نباش، ساده‌ست:

1. **فایل رو باز کن**: برو تو `index-fa.html` یا `index-en.html` و با یه ویرایشگر متن (مثل VSCode یا حتی Notepad) بازش کن.

2. **برو سراغ تابع** `getLaunchDate`: تو بخش `<script>`، این تابع رو پیدا کن:

   ```javascript
   function getLaunchDate() {
       const storedDate = localStorage.getItem('launchDate');
       if (storedDate) {
           return new Date(storedDate);
       } else {
           const newLaunchDate = new Date();
           newLaunchDate.setDate(newLaunchDate.getDate() + 30);
           localStorage.setItem('launchDate', newLaunchDate.toISOString());
           return newLaunchDate;
       }
   }
   ```

3. **زمان رو عوض کن**:

   - اگه می‌خوای مثلاً **10 روز دیگه** باشه:

     ```javascript
     newLaunchDate.setDate(newLaunchDate.getDate() + 10);
     ```

     فقط عدد `30` رو عوض کن با هر چند روزی که می‌خوای (مثل `10`).

   - اگه می‌خوای **یه تاریخ خاص** بذاری (مثل 15 ژوئن 2025):

     ```javascript
     const newLaunchDate = new Date('2025-06-15T00:00:00');
     ```

     تاریخ رو به شکل `YYYY-MM-DDTHH:MM:SS` بنویس (مثل `2025-06-15T00:00:00`).

4. **ذخیره کن**: فایل رو ذخیره کن و تو مرورگر بازش کن. تاریخ جدید تو مرورگر ذخیره می‌شه و تا وقتی کش مرورگرت رو پاک نکنی، همونه.

5. **اگه بخوای تایمر رو ریست کنی**: برو تو کنسول مرورگر (F12 &gt; Console) و اینو بزن:

   ```javascript
   localStorage.removeItem('launchDate');
   ```

   بعد صفحه رو رفرش کن، تایمر با تاریخ جدید شروع می‌شه.

### تصویری از نمونه کد 🖼️

اینجا یه اسکرین‌شات از صفحه وب‌سایت گذاشتم که بتونی ببینی چطور به نظر می‌رسه:

*توجه*: تصویر بالا یه placeholderه. می‌تونی یه اسکرین‌شات از `index-fa.html` یا `index-en.html` بگیری و به اسم `screenshot.png` تو ریپازیتوری آپلود کنی.

---

## English

### Project Overview

This project is a visually appealing "Maintenance" website built using HTML, TailwindCSS, and JavaScript. It is designed to inform users about a website undergoing maintenance and includes the following features:

- **Countdown Timer** ⏳: Displays the time remaining until the site is back online.
- **Newsletter Subscription Form**: Allows users to submit their email for updates.
- **Social Media Links**: Links to social media profiles.
- **Modern Design**: Features a gradient background and smooth animations.
- **Developer Credit**: Includes text "Developed by MmdSrp" and a link to the developer's other projects.

Project files:

- `index-fa.html`: Persian version of the website.
- `index-en.html`: English version of the website.

### How to Set the Countdown Timer

The countdown timer is based on a target date (launchDate) stored in the browser's `localStorage`. To set the timer, you need to edit the JavaScript code in either the Persian (`index-fa.html`) or English (`index-en.html`) file.

1. **Open the File**: Open `index-fa.html` or `index-en.html` in a text editor.

2. **Locate the** `getLaunchDate` **Function**: Find the following function in the `<script>` section:

   ```javascript
   function getLaunchDate() {
       const storedDate = localStorage.getItem('launchDate');
       if (storedDate) {
           return new Date(storedDate);
       } else {
           const newLaunchDate = new Date();
           newLaunchDate.setDate(newLaunchDate.getDate() + 30);
           localStorage.setItem('launchDate', newLaunchDate.toISOString());
           return newLaunchDate;
       }
   }
   ```

3. **Modify the Target Date**:

   - **To set a specific number of days** (e.g., 10 days from now):

     ```javascript
     newLaunchDate.setDate(newLaunchDate.getDate() + 10);
     ```

     Replace `30` with the desired number of days (e.g., `10`).

   - **To set a specific date** (e.g., June 15, 2025):

     ```javascript
     const newLaunchDate = new Date('2025-06-15T00:00:00');
     ```

     Enter the date in the format `YYYY-MM-DDTHH:MM:SS`.

4. **Save Changes**: Save the file and open it in a browser. The new date will be stored in `localStorage` and persist until the browser data is cleared.

5. **Reset the Timer** (Optional): To reset the timer, clear `localStorage`:

   - Open the browser console (F12 &gt; Console) and run:

     ```javascript
     localStorage.removeItem('launchDate');
     ```

   - Refresh the page to start the timer with the new date.

### Sample Code Preview 🖼️

Here's a screenshot of what the website looks like:

*Note*: The image above is a placeholder. You can take a screenshot of `index-fa.html` or `index-en.html` and upload it as `screenshot.png` in the repository.
[Sample Screenshot](https://media.discordapp.net/attachments/1285520019752751108/1366437178300960909/PGTracker.png?ex=68119a0a&is=6810488a&hm=e46257c7e15640d808894ab34e896a14c0b872b5cd0d41bf6bfdd5d5dc2fb334&=&format=webp&quality=lossless&width=538&height=538)

---

Developed by MmdSrp.
