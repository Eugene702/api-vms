# Get Vendor Expert Data – Integrasi PUAS PRO (VMS)

API ini digunakan untuk mengambil daftar **Tenaga Ahli (Vendor Expert)** milik vendor.  
Response sudah disesuaikan untuk kebutuhan **DataTables** pada sisi frontend PUAS PRO.

---

## Endpoint
`GET /api/admin/vendor/vendorExpertData`

---

## Headers
Endpoint ini **wajib menggunakan token hasil login**.
```
Authorization: Bearer {token}
Accept: application/json
```

---

## Payload
Endpoint ini **tidak membutuhkan payload**.

Jika digunakan oleh DataTables, parameter seperti `draw`, `start`, `length`, dan `search`
akan dikirim otomatis sebagai **query parameter**.

---

## Contoh Response Berhasil (200 OK)

```json
{
  "draw": 1,
  "recordsTotal": 4,
  "recordsFiltered": 4,
  "data": [
    {
      "id": 3607,
      "vendor_id": 1,
      "name": "Erling Haaland",
      "gender": "L",
      "dob": "2000-07-21",
      "address": "Leeds, United Kingdom",
      "last_education": "S1",
      "email": "erling.haaland@example.com",
      "expertise": "Software Engineering",
      "nationality": "Norway",
      "work_experience": "5",
      "employee_status": "TETAP",
      "title": "Senior Software Engineer",
      "created_at": "2025-01-15 10:30:00",
      "updated_at": "2026-02-01 14:20:30",
      "action": "<button class='btn btn-sm btn-warning me-1'><i class='fas fa-edit'></i> Edit</button><button class='btn btn-sm btn-danger'><i class='fas fa-trash'></i> Hapus</button>"
    },
    {
      "id": 3608,
      "vendor_id": 1,
      "name": "Kevin De Bruyne",
      "gender": "L",
      "dob": "1991-06-28",
      "address": "Drongen, Belgium",
      "last_education": "S2",
      "email": "kevin.db@example.com",
      "expertise": "Project Management",
      "nationality": "Belgium",
      "work_experience": "10",
      "employee_status": "TETAP",
      "title": "Project Manager",
      "created_at": "2025-01-20 09:15:22",
      "updated_at": "2026-01-30 11:45:10",
      "action": "<button class='btn btn-sm btn-warning me-1'><i class='fas fa-edit'></i> Edit</button><button class='btn btn-sm btn-danger'><i class='fas fa-trash'></i> Hapus</button>"
    },
    {
      "id": 3609,
      "vendor_id": 1,
      "name": "Phil Foden",
      "gender": "L",
      "dob": "2000-05-28",
      "address": "Stockport, England",
      "last_education": "S1",
      "email": "phil.foden@example.com",
      "expertise": "Data Analysis",
      "nationality": "England",
      "work_experience": "3",
      "employee_status": "TIDAK_TETAP",
      "title": "Data Analyst",
      "created_at": "2025-02-10 13:20:45",
      "updated_at": "2026-02-02 08:30:15",
      "action": "<button class='btn btn-sm btn-warning me-1'><i class='fas fa-edit'></i> Edit</button><button class='btn btn-sm btn-danger'><i class='fas fa-trash'></i> Hapus</button>"
    },
    {
      "id": 3610,
      "vendor_id": 1,
      "name": "Bernardo Silva",
      "gender": "L",
      "dob": "1994-08-10",
      "address": "Lisbon, Portugal",
      "last_education": "S1",
      "email": "bernardo.silva@example.com",
      "expertise": "Business Intelligence",
      "nationality": "Portugal",
      "work_experience": "7",
      "employee_status": "TETAP",
      "title": "BI Specialist",
      "created_at": "2025-01-25 16:40:30",
      "updated_at": "2026-02-03 10:15:20",
      "action": "<button class='btn btn-sm btn-warning me-1'><i class='fas fa-edit'></i> Edit</button><button class='btn btn-sm btn-danger'><i class='fas fa-trash'></i> Hapus</button>"
    }
  ]
}
```

---

## Keterangan Field Response

| Field | Tipe | Keterangan |
|-------|------|------------|
| `draw` | integer | Counter untuk DataTables (untuk sinkronisasi request/response) |
| `recordsTotal` | integer | Total seluruh data tanpa filter |
| `recordsFiltered` | integer | Total data setelah filter search (jika ada) |
| `data` | array | Array berisi data tenaga ahli |
| `data[].id` | integer | ID unik tenaga ahli |
| `data[].vendor_id` | integer | ID vendor pemilik tenaga ahli |
| `data[].name` | string | Nama lengkap tenaga ahli |
| `data[].gender` | string | Jenis kelamin (`L` = Laki-laki, `P` = Perempuan) |
| `data[].dob` | date | Tanggal lahir (format: YYYY-MM-DD) |
| `data[].address` | string/null | Alamat lengkap |
| `data[].last_education` | string | Pendidikan terakhir (SD/SMP/SMA/D3/S1/S2/S3) |
| `data[].email` | string | Email tenaga ahli |
| `data[].expertise` | string | Bidang keahlian |
| `data[].nationality` | string | Kewarganegaraan |
| `data[].work_experience` | string | Pengalaman kerja (dalam tahun) |
| `data[].employee_status` | string | Status kepegawaian (`TETAP`/`TIDAK_TETAP`) |
| `data[].title` | string | Jabatan/posisi |
| `data[].created_at` | datetime | Waktu data dibuat |
| `data[].updated_at` | datetime | Waktu data terakhir diupdate |
| `data[].action` | string | HTML button untuk aksi (Edit/Hapus) |

---

## Contoh Response Error (401 Unauthorized)

```json
{
  "message": "Unauthenticated."
}
```

---

## Contoh Response Error (403 Forbidden)

```json
{
  "message": "Akses ditolak. Anda tidak memiliki izin untuk mengakses resource ini."
}
```

---

## Catatan Implementasi

1. **DataTables Integration**: Endpoint ini sudah disesuaikan dengan format response DataTables, sehingga dapat langsung digunakan dengan plugin DataTables di frontend.

2. **Server-Side Processing**: Mendukung server-side processing untuk pagination, sorting, dan searching.

3. **Query Parameters (Opsional)**:
   - `draw` - Counter dari DataTables
   - `start` - Index data awal untuk pagination
   - `length` - Jumlah data per halaman
   - `search[value]` - Keyword untuk pencarian

4. **Action Column**: Field `action` berisi HTML button yang sudah dirender, siap ditampilkan di DataTables.

---

## Contoh Penggunaan dengan DataTables

```javascript
$('#tableVendorExpert').DataTable({
    processing: true,
    serverSide: true,
    ajax: {
        url: '/api/admin/vendor/vendorExpertData',
        headers: {
            'Authorization': 'Bearer ' + token,
            'Accept': 'application/json'
        }
    },
    columns: [
        { data: 'DT_RowIndex', name: 'DT_RowIndex', orderable: false, searchable: false },
        { data: 'name', name: 'name' },
        { data: 'email', name: 'email' },
        { data: 'expertise', name: 'expertise' },
        { data: 'title', name: 'title' },
        { data: 'employee_status', name: 'employee_status' },
        { data: 'work_experience', name: 'work_experience' },
        { data: 'action', name: 'action', orderable: false, searchable: false }
    ]
});
```
