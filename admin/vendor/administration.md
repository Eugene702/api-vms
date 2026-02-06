# Ambil Data Index

API untuk mengambil data Index Administrasi

---

## Endpoint
```
GET /api/admin/vendor/administration
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
        "isVendor": true,
        "vendor": {
            "id": 1,
            "name": "kincat 1",
            "vendor_number": "SI-P-002684.00.00.00",
            "address": "Jl. Dahlia IV No.134 Depok Jaya",
            "city": "depok",
            "postcode": "16432",
            "email": "yohankinata@gmail.com",
            "phone": "02139213",
            "pic_name": "zxc",
            "pic_phone": "123",
            "pic_fax": "123",
            "ratting": "EXCELLENT",
            "rating_score": "120.390625",
            "document_status": "APPROVED",
            "document_status_remark": "saya ubah jadi",
            "document_notes": "{\"SURAT_PERNYATAAN\":{\"status\":\"NO\",\"data\":[]},\"ADMINISTRASI\":{\"status\":\"NO\",\"data\":[]},\"IZIN_USAHA\":{\"status\":\"NO\",\"data\":[]},\"AKTA_PENDIRIAN\":{\"status\":\"NO\",\"data\":[]},\"PENGURUS_PERUSAHAAN\":{\"status\":\"NO\",\"data\":[]},\"KEUANGAN\":{\"status\":\"NO\",\"data\":[]},\"COMPANY_PROFILE\":{\"status\":\"NO\",\"data\":[]},\"TEKNIS\":{\"status\":\"NO\",\"data\":[]} }",
            "bukti_pendukung": "[]",
            "created_at": "2020-07-12 21:27:41",
            "updated_at": "2026-01-28 13:56:57",
            "deleted_at": null,
            "aproval_date": null,
            "need_update_date": null,
            "no_npwp": "123213123",
            "badan_usaha": 1,
            "public_facility": 0,
            "user_id": 2,
            "organization_entity_id": 4,
            "validation_date": null,
            "validation_time": null,
            "validation_other": null,
            "validation_submit": "2024-10-24 11:25:11",
            "active_status": "INACTIVE",
            "approval_status": null,
            "approval_remark": "[{\"action\":\"REJECT_VMS\",\"date\":\"2022-02-12 10:19:35\",\"remark\":\"clean testing data vendor\"}]",
            "inactive_remark": "{\"remark\":\"kakaka\",\"document\":{\"file\":\"project\\/X2ILeA69NiB9K5Ug5UQrpApZfUXRLPUf2sCMhotd.png\",\"datetime\":\"2026-01-28 13:54:42\",\"filename\":\"sample.png\"},\"date\":{\"date\":\"2026-01-28 13:54:41.964737\",\"timezone_type\":3,\"timezone\":\"Asia\\/Jakarta\"}}",
            "is_padi": 0,
            "is_mitra": 1,
            "padi_province_id": "13",
            "padi_city_id": "175",
            "relasi": 0,
            "ips_id": 127,
            "ips_kodeids": "IDS-0001266",
            "deleted": 0
        },
        "organizationTypes": [
            {
                "id": 19,
                "name": "-",
                "created_at": "2021-01-26 17:33:54",
                "updated_at": "2021-01-26 17:33:54"
            },
        ],
        "organizationEntities": [
            {
                "id": 5,
                "name": "BLU/Lem. Pemerintah",
                "created_at": "2021-07-28 11:31:42",
                "updated_at": "2026-01-26 10:03:53"
            },
        ],
        "banks": [
            {
                "id": 83,
                "institution_name": "Bank Aceh Syariah",
                "created_at": "2021-02-03 11:59:00",
                "updated_at": "2021-02-03 11:59:00"
            },
        ],
        "vendorBank": [
            {
                "id": 4824,
                "bank_id": 83,
                "vendor_id": 1,
                "bank": "Bank Aceh Syariah",
                "cabang": "1",
                "rekening": "123",
                "nama": "123",
                "created_at": "2025-10-17 14:36:08",
                "updated_at": "2025-10-17 14:36:08",
                "bank_info": {
                    "id": 83,
                    "institution_name": "Bank Aceh Syariah",
                    "created_at": "2021-02-03 11:59:00",
                    "updated_at": "2021-02-03 11:59:00"
                }
            },
        ],
        "vendorAdministrationExist": true,
        "isFormReadOnly": false,
        "model": {
            "id": 2,
            "vendor_id": "1",
            "vendor_email": "yohankinata@gmail.com",
            "company_name": "kincat 1",
            "company_name_alias": null,
            "organization_type_id": "19",
            "organization_entity_id": 4,
            "province_id": "11",
            "city_id": "1105",
            "district_id": "110501",
            "village_id": "1105012002",
            "address": "Jl. Dahlia IV No.134 Depok Jaya",
            "zip_code": "16432",
            "vendor_stamp_file": "profile/vendor-administration/company-stamp/ZLYWuGHGNYZV8gRlpzod9LC5Qz66F4Ya7388oX50.jpeg",
            "pkp": "Y",
            "pkp_file": "profile/vendor-administration/pkp/lsk24Bbcrngdgps0SReRPXAo5lGzt2JmJvAF8fjb.png",
            "npwp_number": "123213123",
            "nib_number": "1235",
            "npwp_file": "profile/vendor-administration/npwp/SkOBrWrEJM981Wx823OKlMmmstyw5mMjIRxSo9Nl.png",
            "phone_no": "089680667362",
            "fax_no": "123",
            "pic_name": "zxc",
            "pic_phone_no": "123",
            "pic_position": null,
            "company_website": "weqwd",
            "pic_email": "yohankinata@gmail.com",
            "ceo_name": "kincat direktur",
            "office_status": "HEADQUARTER",
            "is_umkm": 0,
            "umkm_category": null,
            "umkm_level": null,
            "is_subsidiary": null,
            "parent_company": null,
            "created_at": "2020-10-12 13:07:12",
            "updated_at": "2025-10-17 14:36:08"
        },
        "isPublicFacility": false,
        "form_validation_source": {
            "organization_type_id": "required",
            "organization_entity_id": "required",
            "province_id": "required",
            "city_id": "required",
            "district_id": "required",
            "village_id": "required",
            "vendor_email": "required",
            "company_name": "required|max:30",
            "address": "required",
            "npwp_number": "required",
            "nib_number": "required",
            "pkp_file": "required",
            "phone_no": "required",
            "pic_name": "required",
            "pic_phone_no": "required",
            "pic_email": "required"
        }
    }
}
```

# Save Data
# End Point
POST /api/admin/vendor/administrationSave

# Payload
```json
{
    // --- FIELD WAJIB UMUM ---
    "organization_type_id": "1",
    "organization_entity_id": "2",
    "province_id": "31",
    "city_id": "3171",
    "district_id": "3171010",
    "village_id": "3171010001",
    
    // --- INFORMASI PERUSAHAAN ---
    "company_name": "PT. Contoh Makmur",
    "vendor_email": "email@unik.com",
    "address": "Jalan Raya No. 1",
    "zip_code": "12345",
    "phone_no": "021123456",
    
    // --- LEGALITAS ---
    "npwp_number": "00.000.000.0-000.000",
    "nib_number": "1234567890",
    
    // --- PERSON IN CHARGE (PIC) ---
    "pic_name": "Budi",
    "pic_phone_no": "08123456789",
    "pic_email": "pic@contoh.com",
    
    // --- FIELD SPESIAL (JSON STRING) ---
    "bankList": "[{\"institution_name\":\"BCA\",\"branch_name\":\"JKT\",\"rekening_no\":\"123\",\"bank_account_name\":\"PT Contoh\"}]",

    "id": "",            // Kosongkan untuk CREATE, isi ID untuk UPDATE
    "vendorId": "",      // Isi jika admin yang menginput user lain
    "isPublicFacility": "0", // 1 atau 0. Jika 1, pic_position WAJIB.

    // --- FIELD FILE (Hanya bisa dikirim via Multipart, tapi key-nya ini) ---
    "vendor_stamp_file": (File),
    "npwp_file": (File),
    "pkp_file": (File)
}

```

# Response
```json
{
    "status": true,
    "message": "Pesan"
}
```