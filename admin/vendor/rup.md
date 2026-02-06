# Ambil Data Table RUP

API untuk mengambil data Table RUP

---

## Endpoint
```
GET /api/admin/vendor/rup/indexData
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
    "draw": 0,
    "recordsTotal": 77,
    "recordsFiltered": 77,
    "data": [
        {
            "id": 590,
            "rup_number": "RUP-2026-02-0005",
            "spph_number": null,
            "kode_investasi": "asass",
            "project_name": "<a target=\"_blank\" href=\"https://rup.kincatonly.com/rup/detail/RUP-2026-02-0005\">test pengadaan</a>",
            "project_type": "GOOD",
            "procurement_group": "INVESTASI",
            "item_type": "Umum",
            "method": "DIRECT",
            "sub_method": null,
            "unit": "SB INFRAS",
            "registration_date": "05/02/2026",
            "registration_date_end": "06/02/2026",
            "items": "[{\"coa_budget\":\"1000000\",\"item_name\":\"aknsa\",\"project_code\":\"COVID-19\",\"budget_utilization\":\"SB INFRAS\",\"directorate_group\":\"COE\",\"quantity\":\"2\",\"volume\":\"2\",\"unit_price\":\"100000\",\"hc_cost\":\"Ya\",\"spesifikasi\":\"kk\"}]",
            "items_final": null,
            "total_amount": "400.000,00",
            "total_final": null,
            "rup_status": "<span class=\"\">Belum Buka</span>",
            "budget_status": "<span class=\"text-danger\">Tertutup</span>",
            "approval_status": "Disetujui GM",
            "reject_remark": "[{\"action\":\"REQUESTED_MANAGER\",\"date\":\"2026-02-05 16:02:51\",\"remark\":null},{\"action\":\"APPROVED_MANAGER\",\"date\":\"2026-02-05 16:03:08\",\"remark\":null},{\"action\":\"APPROVED_GM\",\"date\":\"2026-02-05 16:03:22\",\"remark\":null}]",
            "aproval_manager": "2026-02-05 16:03:08",
            "aproval_gm": "2026-02-05 16:03:22",
            "status_read": "UNREAD",
            "note": null,
            "province_id": 31,
            "city_id": 3101,
            "address": "as",
            "syarat": null,
            "logistik": 0,
            "use_vendor": 0,
            "deleted": 0,
            "deleted_remark": null,
            "created_at": "2026-02-05 13:18:20",
            "updated_at": "2026-02-05 16:03:22",
            "rup_klu": [
                {
                    "id": 212,
                    "rup_id": 590,
                    "klu_id": 2,
                    "created_at": "2026-02-05 13:18:20",
                    "updated_at": "2026-02-05 13:18:20",
                    "klu": {
                        "id": 2,
                        "code": "1c",
                        "name": "PERDAGANGAN BARANG ATK, HASIL CETAKAN DAN PENERBITAN",
                        "description": "Buku, Kertas, ATK lain dan produk-produk hasil percetakan dan penerbitan",
                        "types": "GOOD",
                        "created_at": "2020-07-14 10:52:20",
                        "updated_at": "2021-01-17 17:20:10"
                    }
                }
            ],
            "rup_vendor": [],
            "organization_structure": {
                "id": 1,
                "pengguna_anggaran": "SB INFRAS",
                "siho_cabang_db": "DB INFRAS",
                "status_office": "DIVISI BISNIS",
                "cabang_nav": null,
                "fungsi": "OPERASIONAL",
                "direktorat": "DIRKOM 2",
                "unit_head_ho": "INFRAS",
                "alias_name": null,
                "alamat": "Graha Surveyor Indonesia Lt. 7 Jl. Jend. Gatot Subroto Kav.56 - Jkt - 12950",
                "location": "Jakarta",
                "is_sentralisasi": "1",
                "created_at": "2020-11-19 05:08:10",
                "updated_at": "2020-11-19 05:10:39"
            },
            "location": "Jakarta"
        },
    ],
    "queries": [
        {
            "query": "select count(*) as aggregate from (select * from `rup` where `rup`.`deleted` = ? and exists (select * from `rup_klu` where `rup`.`id` = `rup_klu`.`rup_id` and `klu_id` in (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)) and `approval_status` = ? order by `id` desc) count_row_table",
            "bindings": [],
            "time": 2.75
        },
        {
            "query": "select * from `rup` where `rup`.`deleted` = ? and exists (select * from `rup_klu` where `rup`.`id` = `rup_klu`.`rup_id` and `klu_id` in (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)) and `approval_status` = ? order by `id` desc",
            "bindings": [],
            "time": 3.1
        },
        {
            "query": "select * from `klu` where `klu`.`id` in (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)",
            "bindings": [],
            "time": 1.56
        },
        {
            "query": "select * from `rup_vendor` where `rup_vendor`.`rup_id` in (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)",
            "bindings": [],
            "time": 3.86
        },
        {
            "query": "select * from `master_organization_structure` where `master_organization_structure`.`pengguna_anggaran` in (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)",
            "bindings": [
                "DB INFRAS",
                "DB INS",
                "DB INT",
                "DB MINBA",
                "DB PIK",
                "DB SNE",
                "DHC",
                "DIRKOM",
                "DKA",
                "DKO",
                "DMF",
                "DOP",
                "DTI",
                "SB INFRAS",
                "SB MINBA",
                "SIBAT",
                "SIBLP",
                "SICEH",
                "SIMAK",
                "SIMED",
                "SISMA",
                "SISUB",
                "SPI",
                "STO",
                "UPKBL"
            ],
            "time": 3.52
        }
    ],
    "input": []
}
```