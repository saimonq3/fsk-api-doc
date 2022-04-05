## Описание конечных точек 1С:

##### GET  */api/contragent/* - Запрос контрагентов. В качестве параметров передается пользователь веб-версии, в заголовках передается *Token* авторизации в 1С. В ответ возвращает *JSON* со списком контрагентов конкретного пользователя.

Пример запроса:
> GET /api/contragent/?email=some@mail.ru
Host: 1c-plication.ru
Authorization: Token 7518d22c323ba3ea5b8847e217a44e42785dc4d1
Content-Type: application/json
Accept: */*Accept: */*

Пример ответа:
```json
[
	{
		"uuid": “2108a3a4-0c02-4cf4-ae82-347e9f904eda”,
		"name": "ООО ИнфоСтрой",
	},
	{
		"uuid": “0cbfac04-b60f-465b-b03e-eee3e5d59135”,
		"name": "Ромашка",
	},
	{
		"uuid": “736494a1-2c49-4464-b7f4-7e0c74481917”,
		"name": "Ассорти",
	}
]
```

##### GET */api/contract/* - Запрос договоров пользователя. В качестве параметров передается пользователь веб-версии, в заголовках передается *Token* авторизации в 1С. В ответ возвращает *JSON* со списком контрагентов конкретного пользователя.

Пример запроса:
> GET /api/contract/?email=some@mail.ru
Host: 1c-plication.ru
Authorization: Token 7518d22c323ba3ea5b8847e217a44e42785dc4d1
Content-Type: application/json
Accept: */*

Пример ответа:

```json
[
	{
		"uuid": "736494a1-2c49-4464-b7f4-7e0c74481917",
		"name": "Первый Договор",
		"date": "2022-02-15,
		"company_fsk": "FSK-1",
		"construction_object": {
			"uuid": “7a3ee6d6-b4a5-11ec-b909-0242ac120002”,
			"name": "ул.Гагарина 11, строение 1",
		},
		"company": {
			"uuid": “97887824-b4a5-11ec-b909-0242ac120002”,
			"name": "ООО Ромашка",
		},
		"status": "Активный"},
	{
		"uuid": "ab92f6c8-b4a5-11ec-b909-0242ac120002",
		"name": "Четвертый Договор",
		"date": "2022-02-15,
		"company_fsk": "FSK-2",
		"construction_object": {
			"uuid": “b0321556-b4a5-11ec-b909-0242ac120002”,
			"name": "ул.Мира 15",
		},
		"company": {
			"uuid": “b4f8e4f2-b4a5-11ec-b909-0242ac120002”,
			"name": "ООО Ассорти",
		},
		"status": "Активный"},
{
		"uuid": "ce6f559c-b4a5-11ec-b909-0242ac120002",
		"name": "Второй Договор",
		"date": "2022-02-15,
		"company_fsk": "FSK-3",
		"construction_object": {
			"uuid": “d4aae340-b4a5-11ec-b909-0242ac120002”,
			"name": "ТЦ Алмаз",
		},
		"company": {
			"uuid": “d94adb12-b4a5-11ec-b909-0242ac120002”,
			"name": "ИП Дядя Ваня",
		},
		"status": "Закрыт"},
```

##### GET */api/company-fsk/* - Запрос группы компаний FSK. В заголовках передается *Token* авторизации в 1С. В ответ возвращает *JSON* со списком компаний.

Пример запроса:
> GET /api/company-fsk/
Host: 1c-plication.ru
Authorization: Token 7518d22c323ba3ea5b8847e217a44e42785dc4d1
Content-Type: application/json
Accept: */*

Пример ответа:
```json
[
	{
		"uuid": “2108a3a4-0c02-4cf4-ae82-347e9f904eda”,
		"name": "FSK-1",
	},
	{
		"uuid": “0cbfac04-b60f-465b-b03e-eee3e5d59135”,
		"name": "FSK-2",
	},
	{
		"uuid": “736494a1-2c49-4464-b7f4-7e0c74481917”,
		"name": "FSK-3",
	}
]
```

##### GET */api/constraction-object/* - Запрос объектов строительства. В качестве параметров передается пользователь веб-версии, в заголовках передается *Token* авторизации в 1С. В ответ возвращает *JSON* со списком объектов строительства.

Пример запроса:
> GET /api/constraction-object/?email=some@mail.ru
Host: 1c-plication.ru
Authorization: Token 7518d22c323ba3ea5b8847e217a44e42785dc4d1
Content-Type: application/json
Accept: */*

Пример ответа:
```json
[
	{
		"uuid": “2108a3a4-0c02-4cf4-ae82-347e9f904eda”,
		"name": "ул.Гагарина 11, строение 2",
	},
	{
		"uuid": “0cbfac04-b60f-465b-b03e-eee3e5d59135”,
		"name": "Аквапарк",
	},
	{
		"uuid": “736494a1-2c49-4464-b7f4-7e0c74481917”,
		"name": "ТЦ Алмаз",
	}
]
```

##### GET */api/work-unit/* - Запрос единиц измерения. В заголовках передается *Token* авторизации в 1С. В ответ возвращает *JSON* со списком единиц измерения.

Пример запроса:
> GET /api/work-unit/
Host: 1c-plication.ru
Authorization: Token 7518d22c323ba3ea5b8847e217a44e42785dc4d1
Content-Type: application/json
Accept: */*

Пример ответа:
```json
[
	{
		"uuid": “2108a3a4-0c02-4cf4-ae82-347e9f904eda”,
		"name": "Тонна",
	},
	{
		"uuid": “0cbfac04-b60f-465b-b03e-eee3e5d59135”,
		"name": "Метр",
	},
	{
		"uuid": “736494a1-2c49-4464-b7f4-7e0c74481917”,
		"name": "Килограмм",
	}
]
```

##### GET */api/work-type/* - Запрос типов работ. В заголовках передается *Token* авторизации в 1С. В ответ возвращает *JSON* со списком типов работ.

Пример запроса:
> GET /api/work-type/
Host: 1c-plication.ru
Authorization: Token 7518d22c323ba3ea5b8847e217a44e42785dc4d1
Content-Type: application/json
Accept: */*

Пример ответа:
```json
[
	{
		"uuid": “2108a3a4-0c02-4cf4-ae82-347e9f904eda”,
		"name": "Наименование работы 1",
	},
	{
		"uuid": “0cbfac04-b60f-465b-b03e-eee3e5d59135”,
		"name": "Наименование работы 2",
	},
	{
		"uuid": “736494a1-2c49-4464-b7f4-7e0c74481917”,
		"name": "Наименование работы 3",
	}
]
```

