# Vendor Teknis API

## Endpoint
`GET /admin/vendor/teknis`

## Headers
Accept: application/json
Authorization: Bearer {token}


## Description
Mengambil data teknis vendor meliputi:
- Equipment safety
- Equipment non-safety
- Pengalaman vendor
- Sertifikasi

## Response Example
```json
{
  "status": true,
  "message": "Success",
  "data": {
    "data": {
      "vendorSafetyEquipment": []
    }
  }
}
