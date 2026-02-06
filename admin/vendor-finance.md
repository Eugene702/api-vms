# Get Vendor Data Index

API untuk mengambil data Finance Data Index

---

## Endpoint
```
GET /api/admin/vendor/finance
```

---

## Headers
```
Authorization: Bearer {token}
Accept: application/json
```

---

## Response Berhasil (200 OK)
{
    "status": true,
    "message": "Success",
    "data": {
        "lastFinanceReportYear": [
            "2025",
            "2024",
            "2023"
        ],
        "formKey": [
            {
                "title": "Total Aset Lancar",
                "key": "total_asset_lancar"
            },
            {
                "title": "Total Kewajiban Lancar",
                "key": "total_kewajiban_lancar"
            },
            {
                "title": "Total Aset",
                "key": "total_asset"
            },
            {
                "title": "Total Persediaan",
                "key": "total_persediaan"
            },
            {
                "title": "Total Hutang",
                "key": "total_hutang"
            },
            {
                "title": "Total Ekuitas",
                "key": "total_equity"
            },
            {
                "title": "Total Hutang Jangka Panjang",
                "key": "total_hutang_longterm"
            },
            {
                "title": "Laba Bersih",
                "key": "laba_bersih"
            },
            {
                "title": "Penjualan",
                "key": "sales"
            }
        ],
        "financeReport": {
            "id": 2,
            "vendor_id": 1,
            "total_asset_lancar_third_year": "2017",
            "total_asset_lancar_second_year": "2018",
            "total_asset_lancar_first_year": "2019",
            "total_asset_lancar_third_amount": 3,
            "total_asset_lancar_second_amount": 22,
            "total_asset_lancar_first_amount": 210000,
            "total_kewajiban_lancar_third_year": "2017",
            "total_kewajiban_lancar_second_year": "2018",
            "total_kewajiban_lancar_first_year": "2019",
            "total_kewajiban_lancar_third_amount": 0,
            "total_kewajiban_lancar_second_amount": 0,
            "total_kewajiban_lancar_first_amount": 0,
            "total_asset_third_year": "2017",
            "total_asset_second_year": "2018",
            "total_asset_first_year": "2019",
            "total_asset_third_amount": 0,
            "total_asset_second_amount": 0,
            "total_asset_first_amount": 0,
            "total_persediaan_third_year": "2017",
            "total_persediaan_second_year": "2018",
            "total_persediaan_first_year": "2019",
            "total_persediaan_third_amount": 0,
            "total_persediaan_second_amount": 0,
            "total_persediaan_first_amount": 0,
            "total_hutang_third_year": "2017",
            "total_hutang_second_year": "2018",
            "total_hutang_first_year": "2019",
            "total_hutang_third_amount": 0,
            "total_hutang_second_amount": 0,
            "total_hutang_first_amount": 0,
            "total_equity_third_year": "2017",
            "total_equity_second_year": "2018",
            "total_equity_first_year": "2019",
            "total_equity_third_amount": 0,
            "total_equity_second_amount": 0,
            "total_equity_first_amount": 0,
            "total_hutang_longterm_third_year": "2017",
            "total_hutang_longterm_second_year": "2018",
            "total_hutang_longterm_first_year": "2019",
            "total_hutang_longterm_third_amount": 0,
            "total_hutang_longterm_second_amount": 0,
            "total_hutang_longterm_first_amount": 0,
            "laba_bersih_third_year": "2017",
            "laba_bersih_second_year": "2018",
            "laba_bersih_first_year": "2019",
            "laba_bersih_third_amount": 0,
            "laba_bersih_second_amount": 0,
            "laba_bersih_first_amount": 0,
            "sales_third_year": "2017",
            "sales_second_year": "2018",
            "sales_first_year": "2019",
            "sales_third_amount": 0,
            "sales_second_amount": 0,
            "sales_first_amount": 0,
            "created_at": "2020-08-13 22:06:13",
            "updated_at": "2026-01-31 13:47:22"
        }
    }
}