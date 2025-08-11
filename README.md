# Drug Management Application

## Overview
The Drug Management Application is a desktop-based GUI application developed using Python and Tkinter to manage drug inventory data. It allows users to add, edit, delete, and filter drug records stored in an SQLite database. The application also supports exporting data to Excel and provides a user-friendly interface with Persian localization and date handling using the `tkcalendar` library.

## Features
- **Add/Edit/Delete Records**: Manage drug information including name, count, brand, shape, and expiration date.
- **SQLite Database**: Stores data persistently in a local SQLite database (`drugs.db`).
- **Expiration Date Tracking**: Colors rows based on expiration status (expired, near expiry, warning, safe).
- **Search and Filter**: Search by drug count and filter records by expiration status.
- **Excel Export**: Export drug data to an Excel file with color-coded rows.
- **Persian Localization**: Interface and date handling support Persian language and calendar.
- **Responsive UI**: Built with Tkinter and ttk for a modern and resizable interface.

## Requirements
- Python 3.6+
- Libraries:
  - `tkinter` (included with Python)
  - `sqlite3` (included with Python)
  - `openpyxl` (for Excel export)
  - `tkcalendar` (for Persian calendar support)

To install the required libraries, run:
```bash
pip install openpyxl tkcalendar
```

## Usage
1. Run the application by executing the Python script:
   ```bash
   python drug_management_app.py
   ```
2. Use the input fields to add or edit drug information:
   - **Name**: Drug name (text)
   - **Count**: Drug quantity (numeric)
   - **Brand**: Drug brand (text)
   - **Shape**: Drug type (select from predefined options)
   - **Expiration Date**: Select using the Persian calendar widget
3. Click "ارسال" (Submit) to add a new record or "به‌روزرسانی" (Update) to save changes.
4. Use the search bar to filter records by count.
5. Filter records by expiration status using color-coded buttons.
6. Export data to Excel using the "خروجی Excel" button.
7. Double-click a row to edit or use the "ویرایش ردیف انتخاب شده" button.
8. Delete selected records using the "حذف ردیف انتخاب شده" button.

## File Structure
- `drug_management_app.py`: Main application script.
- `drugs.db`: SQLite database file (created automatically on first run).

## Notes
- The application uses a Persian calendar (`tkcalendar` with `locale='fa_IR'`) for date inputs.
- Rows in the table are color-coded based on expiration:
  - Purple: Expired
  - Red: Expiring within 30 days
  - Orange: Expiring within 90 days
  - Green: Safe (more than 90 days)
- Ensure write permissions in the directory to create and modify `drugs.db` and export Excel files.

## License
This project is licensed under the MIT License.

---

# سامانه مدیریت اطلاعات دارو

## نمای کلی
سامانه مدیریت اطلاعات دارو یک برنامه دسکتاپ با رابط کاربری گرافیکی است که با استفاده از پایتون و Tkinter توسعه یافته است. این برنامه برای مدیریت داده‌های موجودی دارو طراحی شده و امکان افزودن، ویرایش، حذف و فیلتر کردن سوابق دارو را در یک پایگاه داده SQLite فراهم می‌کند. همچنین، این برنامه از صدور داده‌ها به فرمت اکسل پشتیبانی می‌کند و رابط کاربری ساده‌ای با پشتیبانی از زبان پارسی و تقویم پارسی ارائه می‌دهد.

## ویژگی‌ها
- **افزودن/ویرایش/حذف سوابق**: مدیریت اطلاعات دارو شامل نام، تعداد، برند، نوع و تاریخ انقضا.
- **پایگاه داده SQLite**: ذخیره داده‌ها به صورت دائمی در پایگاه داده محلی (`drugs.db`).
- **پیگیری تاریخ انقضا**: رنگ‌آمیزی ردیف‌ها بر اساس وضعیت انقضا (منقضی، نزدیک به انقضا، هشدار، ایمن).
- **جستجو و فیلتر**: جستجو بر اساس تعداد دارو و فیلتر کردن سوابق بر اساس وضعیت انقضا.
- **صدور به اکسل**: صدور داده‌های دارو به فایل اکسل با ردیف‌های رنگی.
- **پشتیبانی از زبان پارسی**: رابط کاربری و مدیریت تاریخ با پشتیبانی از زبان و تقویم پارسی.
- **رابط کاربری پاسخ‌گو**: ساخته شده با Tkinter و ttk برای رابط کاربری مدرن و قابل تغییر اندازه.

## پیش‌نیازها
- پایتون نسخه 3.6 یا بالاتر
- کتابخانه‌ها:
  - `tkinter` (به صورت پیش‌فرض با پایتون ارائه می‌شود)
  - `sqlite3` (به صورت پیش‌فرض با پایتون ارائه می‌شود)
  - `openpyxl` (برای صدور به اکسل)
  - `tkcalendar` (برای پشتیبانی از تقویم پارسی)

برای نصب کتابخانه‌های مورد نیاز، دستور زیر را اجرا کنید:
```bash
pip install openpyxl tkcalendar
```

## نحوه استفاده
1. برنامه را با اجرای اسکریپت پایتون راه‌اندازی کنید:
   ```bash
   python drug_management_app.py
   ```
2. از فیلدهای ورودی برای افزودن یا ویرایش اطلاعات دارو استفاده کنید:
   - **نام**: نام دارو (متن)
   - **تعداد**: تعداد دارو (عدد)
   - **برند**: برند دارو (متن)
   - **نوع**: نوع دارو (انتخاب از گزینه‌های از پیش تعیین شده)
   - **تاریخ انقضا**: انتخاب با استفاده از ویجت تقویم پارسی
3. روی دکمه "ارسال" برای افزودن رکورد جدید یا "به‌روزرسانی" برای ذخیره تغییرات کلیک کنید.
4. از نوار جستجو برای فیلتر کردن سوابق بر اساس تعداد استفاده کنید.
5. سوابق را بر اساس وضعیت انقضا با دکمه‌های رنگی فیلتر کنید.
6. داده‌ها را با دکمه "خروجی Excel" به اکسل صادر کنید.
7. برای ویرایش، روی یک ردیف دوبار کلیک کنید یا از دکمه "ویرایش ردیف انتخاب شده" استفاده کنید.
8. سوابق انتخاب شده را با دکمه "حذف ردیف انتخاب شده" حذف کنید.

## ساختار فایل‌ها
- `drug_management_app.py`: اسکریپت اصلی برنامه.
- `drugs.db`: فایل پایگاه داده SQLite (به طور خودکار در اولین اجرا ایجاد می‌شود).

## نکات
- برنامه از تقویم پارسی (`tkcalendar` با `locale='fa_IR'`) برای ورودی‌های تاریخ استفاده می‌کند.
- ردیف‌های جدول بر اساس وضعیت انقضا رنگ‌آمیزی می‌شوند:
  - بنفش: منقضی شده
  - قرمز: در حال انقضا در 30 روز آینده
  - نارنجی: در حال انقضا در 90 روز آینده
  - سبز: ایمن (بیش از 90 روز)
- اطمینان حاصل کنید که مجوزهای نوشتن در دایرکتوری برای ایجاد و تغییر `drugs.db` و صدور فایل‌های اکسل وجود دارد.

## مجوز
این پروژه تحت مجوز MIT منتشر شده است.

---

# 药品管理应用程序

## 概述
药品管理应用程序是一个基于桌面的图形用户界面应用程序，使用 Python 和 Tkinter 开发，用于管理药品库存数据。它允许用户在 SQLite 数据库中添加、编辑、删除和过滤药品记录。该应用程序还支持将数据导出到 Excel，并提供支持波斯语本地化和使用 `tkcalendar` 库进行日期处理的友好用户界面。

## 功能
- **添加/编辑/删除记录**：管理药品信息，包括名称、数量、品牌、类型和到期日期。
- **SQLite 数据库**：在本地 SQLite 数据库（`drugs.db`）中持久存储数据。
- **到期日期跟踪**：根据到期状态对行进行着色（已过期、即将过期、警告、安全）。
- **搜索和过滤**：按药品数量搜索记录，并按到期状态过滤记录。
- **Excel 导出**：将药品数据导出为带有颜色编码行的 Excel 文件。
- **波斯语本地化**：界面和日期处理支持波斯语和波斯历。
- **响应式用户界面**：使用 Tkinter 和 ttk 构建现代且可调整大小的界面。

## 要求
- Python 3.6 或更高版本
- 库：
  - `tkinter`（Python 自带）
  - `sqlite3`（Python 自带）
  - `openpyxl`（用于 Excel 导出）
  - `tkcalendar`（用于支持波斯历）

安装所需库的命令：
```bash
pip install openpyxl tkcalendar
```

## 使用方法
1. 通过运行 Python 脚本启动应用程序：
   ```bash
   python drug_management_app.py
   ```
2. 使用输入字段添加或编辑药品信息：
   - **名称**：药品名称（文本）
   - **数量**：药品数量（数字）
   - **品牌**：药品品牌（文本）
   - **类型**：药品类型（从预定义选项中选择）
   - **到期日期**：使用波斯历小部件选择
3. 点击“提交”按钮添加新记录，或“更新”按钮保存更改。
4. 使用搜索栏按数量过滤记录。
5. 使用颜色编码按钮按到期状态过滤记录。
6. 使用“导出 Excel”按钮将数据导出到 Excel。
7. 双击一行进行编辑，或使用“编辑选中行”按钮。
8. 使用“删除选中行”按钮删除选中的记录。

## 文件结构
- `drug_management_app.py`：主应用程序脚本。
- `drugs.db`：SQLite 数据库文件（首次运行时自动创建）。

## 注意事项
- 应用程序使用波斯历（`tkcalendar` 设置为 `locale='fa_IR'`）进行日期输入。
- 表格中的行根据到期状态进行颜色编码：
  - 紫色：已过期
  - 红色：30 天内即将过期
  - 橙色：90 天内即将过期
  - 绿色：安全（超过 90 天）
- 确保目录具有写权限，以便创建和修改 `drugs.db` 以及导出 Excel 文件。

## 许可证
本项目采用 MIT 许可证。