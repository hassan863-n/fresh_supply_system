# FreshSupply Core - نظام إدارة وتتبع سلاسل الإمداد والتخزين الذكي للمنتجات الطازجة

## نظرة عامة
واجهة برمجية (Backend) مبنية باستخدام **Python FastAPI** لإدارة مستودعات المنتجات الطازجة، تتبع الصلاحية ودرجات الحرارة، إدارة الشحنات، وإصدار تقارير التلف التلقائي مع نظام صلاحيات للمستخدمين (RBAC).

## هيكل المشروع
- `core/`: الإعدادات العامة وقاعدة البيانات (`config.py`, `database.py`).
- `models/`: نماذج قاعدة البيانات (`user.py`, `product.py`, `shipment.py`).
- `schemas/`: مخططات التحقق من البيانات (`user_schema.py`, `product_schema.py`, `shipment_schema.py`).
- `services/`: منطق الأعمال (`auth_service.py`, `inventory_service.py`, `logistic_service.py`).
- `routers/`: نقاط النهاية للواجهة البرمجية (`auth.py`, `inventory.py`, `shipments.py`).
- `tests/`: اختبارات الوحدة والتكامل (`test_inventory.py`, `test_shipments.py`).
- `docs/`: وثائق المتطلبات والمخططات المعمارية (SRS, Use Case, Sequence Diagram).

## طريقة التشغيل
1. تثبيت المكتبات:
```bash
pip install -r requirements.txt
```
2. تشغيل الخادم:
```bash
uvicorn main:app --reload
```
3. فتح صفحة التوثيق التفاعلية (Swagger UI):
افتح المتصفح على الرابط: `http://127.0.0.1:8000/docs`

4. تشغيل الاختبارات:
```bash
python -m pytest
```
