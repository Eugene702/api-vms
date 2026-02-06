# Get Vendor Technical Data

API untuk mengambil data teknis vendor (Peralatan Safety, Non-Safety, Pengalaman, dan Sertifikasi).

---

## Endpoint
```
GET /api/admin/vendor/teknis
```

---

## Headers
```
Authorization: Bearer {token}
Accept: application/json
```

---

## Response Berhasil (200 OK)

```json
{
  "status": true,
  "message": "Success",
  "data": {
    "data": {
      "vendorSafetyEquipment": [
        {
          "id": 844,
          "vendor_id": 1,
          "name": "Safety Helmet",
          "ownership_proof": "LP01223",
          "type": "MSA V-Gard",
          "creation_date": "2021",
          "ownership_status": "MILIK_SENDIRI",
          "amount": "50",
          "capacity": "Standard",
          "file": "teknis/equipment/safety/safety-helmet.pdf",
          "location": "Jakarta",
          "condition": "Baik",
          "created_at": "2025-01-10 10:00:00",
          "updated_at": "2026-02-01 14:30:00"
        },
        {
          "id": 845,
          "vendor_id": 1,
          "name": "Safety Shoes",
          "ownership_proof": "LP01224",
          "type": "King's KWD 901",
          "creation_date": "2022",
          "ownership_status": "MILIK_SENDIRI",
          "amount": "100",
          "capacity": "Size 39-44",
          "file": "teknis/equipment/safety/safety-shoes.pdf",
          "location": "Jakarta",
          "condition": "Baik",
          "created_at": "2025-01-10 10:05:00",
          "updated_at": "2026-02-01 14:35:00"
        }
      ],
      "vendorNonSafetyEquipment": [
        {
          "id": 1190,
          "vendor_id": 1,
          "name": "Laptop",
          "ownership_proof": "B002",
          "type": "Dell Latitude 5420",
          "creation_date": "2023",
          "ownership_status": "SEWA",
          "amount": "25",
          "capacity": "Intel i7, 16GB RAM",
          "file": "teknis/equipment/non-safety/laptop.pdf",
          "location": "Jakarta",
          "condition": "Sangat Baik",
          "created_at": "2025-01-15 11:00:00",
          "updated_at": "2026-02-02 15:20:00"
        },
        {
          "id": 1191,
          "vendor_id": 1,
          "name": "Proyektor",
          "ownership_proof": "B003",
          "type": "Epson EB-X05",
          "creation_date": "2022",
          "ownership_status": "MILIK_SENDIRI",
          "amount": "5",
          "capacity": "3300 Lumens",
          "file": "teknis/equipment/non-safety/projector.pdf",
          "location": "Bandung",
          "condition": "Baik",
          "created_at": "2025-01-16 09:30:00",
          "updated_at": "2026-02-02 16:00:00"
        }
      ],
      "vendorExperience": [
        {
          "id": 2257,
          "vendor_id": 1,
          "contract_name": "Pengadaan Infrastruktur IT",
          "institution_name": "PT Telkom Indonesia",
          "phone_no": "021-54321000",
          "contract_amount": "5000000000",
          "bast_date": "2024-12-31",
          "location": "Jakarta",
          "address": "Jl. Gatot Subroto Kav. 52, Jakarta",
          "contract_no": "PKS/2023/001",
          "contract_date": "2023-01-15",
          "contract_end_date": "2024-12-31",
          "realization_percentage": "100",
          "contract_file": "teknis/experiences/past/telkom-contract.pdf",
          "description": "Proyek selesai dengan baik",
          "created_at": "2025-01-20 10:00:00",
          "updated_at": "2025-01-20 10:00:00"
        },
        {
          "id": 2258,
          "vendor_id": 1,
          "contract_name": "Pembangunan Sistem Informasi",
          "institution_name": "Bank Mandiri",
          "phone_no": "021-52997777",
          "contract_amount": "8000000000",
          "bast_date": "2023-11-30",
          "location": "Jakarta",
          "address": "Jl. Jend. Gatot Subroto Kav. 36-38, Jakarta",
          "contract_no": "PKS/2022/045",
          "contract_date": "2022-03-01",
          "contract_end_date": "2023-11-30",
          "realization_percentage": "100",
          "contract_file": "teknis/experiences/past/mandiri-contract.pdf",
          "description": "Implementasi sukses",
          "created_at": "2025-01-21 11:00:00",
          "updated_at": "2025-01-21 11:00:00"
        }
      ],
      "vendorExperienceOnGoing": [
        {
          "id": 1,
          "vendor_id": 1,
          "contract_name": "Pengembangan Platform Digital",
          "institution_name": "PT Astra International",
          "phone_no": "021-65866666",
          "contract_amount": "12000000000",
          "bast_date": null,
          "location": "Jakarta",
          "address": "Jl. Gaya Motor Raya No. 8, Sunter II, Jakarta",
          "contract_no": "PKS/2025/012",
          "contract_date": "2025-02-01",
          "contract_end_date": "2026-12-31",
          "realization_percentage": "35",
          "contract_file": "teknis/experiences/on-going/astra-contract.pdf",
          "description": "Dalam proses pengembangan tahap 2",
          "created_at": "2025-02-05 14:00:00",
          "updated_at": "2026-02-05 10:30:00"
        },
        {
          "id": 2,
          "vendor_id": 1,
          "contract_name": "Modernisasi Infrastruktur Jaringan",
          "institution_name": "Kementerian Keuangan RI",
          "phone_no": "021-3449230",
          "contract_amount": "15000000000",
          "bast_date": null,
          "location": "Jakarta",
          "address": "Jl. Dr. Wahidin Raya No. 1, Jakarta",
          "contract_no": "PKS/2024/089",
          "contract_date": "2024-06-01",
          "contract_end_date": "2026-06-30",
          "realization_percentage": "60",
          "contract_file": "teknis/experiences/on-going/kemenkeu-contract.pdf",
          "description": "Progres berjalan sesuai timeline",
          "created_at": "2024-06-10 09:00:00",
          "updated_at": "2026-02-04 16:00:00"
        }
      ],
      "vendorCertification": [
        {
          "id": 850,
          "vendor_id": 1,
          "file": "teknis/certifications/iso-9001.pdf",
          "start_date": "2024-01-01",
          "end_date": "2027-01-01",
          "description": "ISO 9001:2015 Quality Management System",
          "created_at": "2024-01-15 10:00:00",
          "updated_at": "2024-01-15 10:00:00"
        },
        {
          "id": 851,
          "vendor_id": 1,
          "file": "teknis/certifications/iso-27001.pdf",
          "start_date": "2024-03-01",
          "end_date": "2027-03-01",
          "description": "ISO/IEC 27001:2013 Information Security Management",
          "created_at": "2024-03-20 11:30:00",
          "updated_at": "2024-03-20 11:30:00"
        },
        {
          "id": 852,
          "vendor_id": 1,
          "file": "teknis/certifications/sbu.pdf",
          "start_date": "2025-01-01",
          "end_date": "2028-01-01",
          "description": "Sertifikat Badan Usaha (SBU) Konstruksi - Grade 7",
          "created_at": "2025-01-10 14:00:00",
          "updated_at": "2025-01-10 14:00:00"
        }
      ]
    }
  }
}
```
