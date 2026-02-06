# Get Vendor Expert Data – Integrasi PUAS PRO (VMS)

API ini digunakan untuk mengambil daftar **Tenaga Ahli (Vendor Expert)** milik vendor.  
Response sudah disesuaikan untuk kebutuhan **DataTables** pada sisi frontend PUAS PRO.

---

## Endpoint
`GET /api/admin/vendor/vendorExpertData`

---

## Headers
Endpoint ini **wajib menggunakan token hasil login**.
Authorization: Bearer {token}
Accept: application/json


---

## Payload
Endpoint ini **tidak membutuhkan payload**.

Jika digunakan oleh DataTables, parameter seperti `draw`, `start`, `length`, dan `search`
akan dikirim otomatis sebagai **query parameter**.

---

## Contoh Response Berhasil (200 OK)

```json
{
  "draw": 0,
  "recordsTotal": 4,
  "recordsFiltered": 4,
  "data": [
    {
      "id": 3607,
      "vendor_id": 1,
      "name": "Erling",
      "gender": "L",
      "dob": "2025-12-01",
      "address": null,
      "last_education": "SD",
      "email": "jim@mail.co",
      "expertise": "Striker",
      "nationality": "UK",
      "work_experience": "2",
      "employee_status": "TIDAK_TETAP",
      "title": "Striker",
      "created_at": "2026-02-01 23:27:17",
      "updated_at": "2026-02-01 23:27:17",
      "action": "<button class='btn btn-sm btn-primary'>Edit</button>"
    }
  ]
}