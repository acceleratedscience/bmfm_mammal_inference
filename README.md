# bmfm_mammal_inference

Dev note:

Testing during development:

POST to http://0.0.0.0:8080/service

This input to dti:
```json
{
    "service_type": "get_protein_property",
    "service_name": "get protein dti",
    "parameters": {
        "property_type": [
            "dti"
        ],
        "subjects": [
          "NLMKRCTRGFRKLGKCTTLEEEKCKTLYPRGQCTCSDSKMNTHSCDCKSC"
        ],
			  "drug_smiles": "'CC(=O)NCCC1=CNc2c1cc(OC)cc2'"
    }
}
```

Returns this dti value:
```json
[
	{
		"subject": "NLMKRCTRGFRKLGKCTTLEEEKCKTLYPRGQCTCSDSKMNTHSCDCKSC",
		"property": "dti",
		"result": 4.042873859405518
	}
]
```

This sol input:
```json
{
    "service_type": "get_protein_property",
    "service_name": "get protein sol",
    "parameters": {
        "property_type": [
            "sol"
        ],
        "subjects": [
          "NLMKRCTRGFRKLGKCTTLEEEKCKTLYPRGQCTCSDSKMNTHSCDCKSC"
        ]
    }
}
```

... returns this sol output:
```json
[
	{
		"subject": "NLMKRCTRGFRKLGKCTTLEEEKCKTLYPRGQCTCSDSKMNTHSCDCKSC",
		"property": "sol",
		"result": 1
	}
]
```
