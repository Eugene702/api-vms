# Get Vendor Technical Data

API ini digunakan untuk mengambil **data teknis vendor**, meliputi:
- Peralatan Safety
- Peralatan Non-Safety
- Pengalaman Vendor (Selesai & Berjalan)
- Sertifikasi Vendor

API ini biasanya digunakan untuk halaman **Profil Teknis Vendor**.

---

## Endpoint
`GET /api/admin/vendor/teknis`

---

## Headers
Endpoint ini **wajib autentikasi** menggunakan token hasil login.
Authorization: Bearer {token}
Accept: application/json


---

## Payload
Endpoint ini **tidak membutuhkan payload**.

---

## Contoh Response Berhasil (200 OK)

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
          "name": "Tablet",
          "ownership_proof": "LP01223",
          "type": "SONY",
          "creation_date": "2021",
          "ownership_status": "SEWA",
          "amount": "231",
          "capacity": "90 / RAM 102",
          "file": "teknis/equipment/safety/MipZyjiPgIqOwT18HB0HdBr9WpFGPg8au0m6Vxfq.pdf",
          "location": "JKT",
          "condition": "25",
          "created_at": "2026-02-02 22:05:17",
          "updated_at": "2026-02-02 22:05:17"
        }
      ],
      "vendorNonSafetyEquipment": [
        {
          "id": 1190,
          "vendor_id": 1,
          "name": "BUKU",
          "ownership_proof": "B002",
          "type": "Kiky",
          "creation_date": "2002",
          "ownership_status": "SEWA",
          "amount": "23",
          "capacity": "Kertas",
          "file": "teknis/equipment/non-safety/8QZeCxGOjFk7ajby6X1Me5icfR0szGUcpOm6JkDv.pdf",
          "location": "JKT",
          "condition": "99",
          "created_at": "2026-02-02 22:14:23",
          "updated_at": "2026-02-02 22:14:23"
        }
      ],
      "vendorExperience": [
        {
          "id": 2257,
          "vendor_id": 1,
          "contract_name": "pengadaan mobil hybrid",
          "institution_name": "Elon musk",
          "phone_no": "120390129309",
          "contract_amount": "10000000000",
          "bast_date": "2026-02-28",
          "location": "Jawa Barat",
          "address": "USA",
          "contract_no": "1230912039",
          "contract_date": "2026-02-28",
          "contract_end_date": "2026-02-28",
          "realization_percentage": "10",
          "contract_file": "teknis/experiences/past/4IZGPAeXjh9KehatRw2E16NqFygQvUogBoaL2g7Q.pdf",
          "description": "testing",
          "created_at": "2026-02-03 22:09:51",
          "updated_at": "2026-02-03 22:09:51"
        }
      ],
      "vendorExperienceOnGoing": [
        {
          "id": 1,
          "vendor_id": 1,
          "contract_name": "Proyek Pengadaan PCI",
          "institution_name": "Indofood",
          "phone_no": "021-121212",
          "contract_amount": "25000000",
          "bast_date": "2020-07-07",
          "location": "Semarang",
          "address": "Jalan Tembalang",
          "contract_no": "1231231233",
          "contract_date": "2018-07-28",
          "contract_end_date": "2020-04-07",
          "realization_percentage": "99",
          "contract_file": "teknis/experiences/on-going/KXZBpGiI7iT3BwUH0Pl0wVwVwKs8lSNa9RcYai3I.png",
          "description": "Selesai",
          "created_at": "2020-07-27 15:03:17",
          "updated_at": "2020-07-29 23:02:43"
        }
      ],
      "vendorCertification": [
        {
          "id": 850,
          "vendor_id": 1,
          "file": "teknis/certifications/RwcZyIwwHjYasV0tkBClWvDjBWfmT94vI1GqL98S.pdf",
          "start_date": "2026-02-01",
          "end_date": "2026-02-04",
          "description": "ISO3",
          "created_at": "2026-02-01 23:39:00",
          "updated_at": "2026-02-01 23:39:00"
        }
      ]
    }
  }
}
