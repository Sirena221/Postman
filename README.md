# Postman
{
	"info": {
		"_postman_id": "ac8ef771-7a48-4b83-9c62-61f32cfe3ed3",
		"name": "Yandex.prilavok",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "24060512"
	},
	"item": [
		{
			"name": "Получить список наборов в карточке",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"method": "GET",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits?cardId=1",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits"
					],
					"query": [
						{
							"key": "cardId",
							"value": "1"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Создать пустой набор",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"cardId\": 1, \r\n    \"name\": \"В космос\" \r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits"
					]
				}
			},
			"response": []
		},
		{
			"name": "Получить список наборов по продуктам",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"ids\": [\r\n        1,\r\n        22\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/products/kits",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"products",
						"kits"
					]
				}
			},
			"response": []
		},
		{
			"name": "Получить список продуктов по имени набора",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{server_url}}api/v1/kits/search?name=В+космос",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits",
						"search"
					],
					"query": [
						{
							"key": "name",
							"value": "В+космос"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Sozdat' pustoy nabor lepim pelmeni",
			"request": {
				"method": "POST",
				"header": [
					{
						"key": "Content-Type",
						"value": "application/json"
					}
				],
				"body": {
					"mode": "raw",
					"raw": "{cardId: 1, \"name\": \"Лепим пельмени\"} "
				},
				"url": {
					"raw": "https://87b1dbd9-237f-452d-bb79-f954d78db8d6.serverhub.praktikum-services.ru/api/v1/kits",
					"protocol": "https",
					"host": [
						"87b1dbd9-237f-452d-bb79-f954d78db8d6",
						"serverhub",
						"praktikum-services",
						"ru"
					],
					"path": [
						"api",
						"v1",
						"kits"
					]
				}
			},
			"response": []
		},
		{
			"name": "izmenit imya nobora",
			"request": {
				"method": "PUT",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"name\": \"Переименованный набор\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "https://7c13d818-5d72-45a7-a430-d1e87ef30279.serverhub.praktikum-services.ru/api/v1/kits/:id",
					"protocol": "https",
					"host": [
						"7c13d818-5d72-45a7-a430-d1e87ef30279",
						"serverhub",
						"praktikum-services",
						"ru"
					],
					"path": [
						"api",
						"v1",
						"kits",
						":id"
					],
					"variable": [
						{
							"key": "id",
							"value": "7"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "udalit' nabor",
			"request": {
				"method": "DELETE",
				"header": [],
				"url": {
					"raw": "https://7c13d818-5d72-45a7-a430-d1e87ef30279.serverhub.praktikum-services.ru/api/v1/kits/:id",
					"protocol": "https",
					"host": [
						"7c13d818-5d72-45a7-a430-d1e87ef30279",
						"serverhub",
						"praktikum-services",
						"ru"
					],
					"path": [
						"api",
						"v1",
						"kits",
						":id"
					],
					"variable": [
						{
							"key": "id",
							"value": "7"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Получить все логи сервера Яндекс.Прилавок",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{server_url}}api/logs/main",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"logs",
						"main"
					]
				}
			},
			"response": []
		},
		{
			"name": "Проверить стоимость доставки Яндекс.Прилавок",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n\"products\": [\r\n{\"id\": 1, \"quantity\": 3}\r\n],\r\n\"deliveryTime\": 6\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/couriers/check",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"couriers",
						"check"
					]
				}
			},
			"response": []
		},
		{
			"name": "Проверить наличие товаров на складах Яндекс.Прилавок",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"products\": [\r\n        {\r\n            \"id\": 5,\r\n            \"quantity\": 1\r\n        },\r\n        {\r\n            \"id\": 4,\r\n            \"quantity\": 5\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/warehouses/check",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"warehouses",
						"check"
					]
				}
			},
			"response": []
		},
		{
			"name": "получить логи по складам",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{server_url}}api/logs/secondary",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"logs",
						"secondary"
					]
				}
			},
			"response": []
		},
		{
			"name": "Добавить продукты в набор Яндекс.Прилавок",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": 61,\r\n            \"quantity\": 2\r\n        },\r\n        {\r\n            \"id\": 10,\r\n            \"quantity\": 2\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits/:id/products",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits",
						":id",
						"products"
					],
					"variable": [
						{
							"key": "id",
							"value": "5"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Добавить продукты в набор Яндекс.Прилавок 2",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": 45,\r\n            \"quantity\": 2\r\n        },\r\n        {\r\n            \"id\": 3,\r\n            \"quantity\": 2\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits/:id/products",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits",
						":id",
						"products"
					],
					"variable": [
						{
							"key": "id",
							"value": "2"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Поиск наборов по продуктам",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"ids\": [\r\n        39,\r\n        34\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/products/kits",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"products",
						"kits"
					]
				}
			},
			"response": []
		},
		{
			"name": "проверить, есть ли продукты на складе «Чердак»",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\r\n<InputModel>\r\n    <deliveryTime>9</deliveryTime>\r\n    <product id=\"4\" quantity=\"2\" />\r\n    <product id=\"48\" quantity=\"2\" />\r\n</InputModel>",
					"options": {
						"raw": {
							"language": "xml"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}attic/calculate.xml",
					"host": [
						"{{server_url}}attic"
					],
					"path": [
						"calculate.xml"
					]
				}
			},
			"response": []
		},
		{
			"name": "проверить, есть ли продукты на складе «Большой мир».",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "<?xml version=\"1.0\" encoding=\"utf-8\"?>\r\n<soap:Envelope xmlns:soap=\"http://schemas.xmlsoap.org/soap/envelope/\" xmlns:xsi=\"http://www.w3.org/2001/XMLSchema-instance\"  xmlns:tns=\"WebServices.WarehouseWsdl\">\r\n    <soap:Body>\r\n        <tns:checkSupply>\r\n            <tns:products>\r\n                <tns:products>\r\n                    <id>2</id>\r\n                    <quantity>1</quantity>\r\n                </tns:products>\r\n                <tns:products>\r\n                    <id>49</id>\r\n                    <quantity>1</quantity>\r\n                </tns:products>\r\n            </tns:products>\r\n            <tns:deliveryTime>10</tns:deliveryTime>\r\n        </tns:checkSupply>\r\n    </soap:Body>\r\n</soap:Envelope>",
					"options": {
						"raw": {
							"language": "xml"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}big-world/wsdl",
					"host": [
						"{{server_url}}big-world"
					],
					"path": [
						"wsdl"
					]
				}
			},
			"response": []
		},
		{
			"name": "registrazia name positiv",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"firstName\": \"Леонид\",\r\n    \"phone\": \"+89998887766\",\r\n    \"address\": \"г. Москва, ул. Ленина, д. 1, кв. 6\",\r\n    \"email\": \"leonid@yandex.ru\",\r\n    \"comment\": \"Звонить в домофон\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/users",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"users"
					]
				}
			},
			"response": []
		},
		{
			"name": "registrazia name negativ",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"firstName\": \"Л\",\r\n    \"phone\": \"+89998887766\",\r\n    \"address\": \"г. Москва, ул. Ленина, д. 1, кв. 6\",\r\n    \"email\": \"leonid@yandex.ru\",\r\n    \"comment\": \"Звонить в домофон\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/users",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"users"
					]
				}
			},
			"response": []
		},
		{
			"name": "registrazia telephone negativ",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"firstName\": \"Леонид\",\r\n    \"phone\": \"\",\r\n    \"address\": \"г. Москва, ул. Ленина, д. 1, кв. 6\",\r\n    \"email\": \"leonid@yandex.ru\",\r\n    \"comment\": \"Звонить в домофон\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/users",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"users"
					]
				}
			},
			"response": []
		},
		{
			"name": "registrazia telephone negativ2",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"firstName\": \"Леонид\",\r\n    \"phone\": \"89998887766\",\r\n    \"address\": \"г. Москва, ул. Ленина, д. 1, кв. 6\",\r\n    \"email\": \"leonid@yandex.ru\",\r\n    \"comment\": \"Звонить в домофон\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/users",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"users"
					]
				}
			},
			"response": []
		},
		{
			"name": "registrazia telephone negativ3",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"firstName\": \"Леонид\",\r\n    \"phone\": \"+899988877661\",\r\n    \"address\": \"г. Москва, ул. Ленина, д. 1, кв. 6\",\r\n    \"email\": \"leonid@yandex.ru\",\r\n    \"comment\": \"Звонить в домофон\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/users",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"users"
					]
				}
			},
			"response": []
		},
		{
			"name": "Создать пустой набор Спортивный",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"cardId\": 1, \r\n    \"name\": \"Спортивный\" \r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits"
					]
				}
			},
			"response": []
		},
		{
			"name": "получить список наборов",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{server_url}}api/v1/kits?cardId=1",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits"
					],
					"query": [
						{
							"key": "cardId",
							"value": "1"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Добавить продукты в набор Спортивный",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": 1,\r\n            \"quantity\": 1\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits/:id/products",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits",
						":id",
						"products"
					],
					"variable": [
						{
							"key": "id",
							"value": "7"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Добавить продукты в набор Спортивный 1.2",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": 1.2,\r\n            \"quantity\": 1\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits/:id/products",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits",
						":id",
						"products"
					],
					"variable": [
						{
							"key": "id",
							"value": "7"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Добавить продукты в набор Спортивный \"Апр\"",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": \"Апр\",\r\n            \"quantity\": 1\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/kits/:id/products",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"kits",
						":id",
						"products"
					],
					"variable": [
						{
							"key": "id",
							"value": "7"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "проверить, есть ли доставка курьерской службой «Привезём быстро» и сколько она стоит",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "<InputModel>\r\n    <productsCount>8</productsCount>\r\n    <productsWeight>5</productsWeight>\r\n    <deliveryTime>20</deliveryTime>\r\n</InputModel>",
					"options": {
						"raw": {
							"language": "xml"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}fast-delivery/v3.1.1/calculate-delivery.xml",
					"host": [
						"{{server_url}}fast-delivery"
					],
					"path": [
						"v3.1.1",
						"calculate-delivery.xml"
					]
				}
			},
			"response": []
		},
		{
			"name": "Создание корзина",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": 1,\r\n            \"quantity\": 1\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/orders",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"orders"
					]
				}
			},
			"response": []
		},
		{
			"name": "Получение списка продуктов в корзине",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "{{server_url}}api/v1/orders/:id",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"orders",
						":id"
					],
					"variable": [
						{
							"key": "id",
							"value": "2"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "добавление продуктов в корзину",
			"request": {
				"method": "PUT",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"productsList\": [\r\n        {\r\n            \"id\": 4,\r\n            \"quantity\": 1\r\n        },\r\n        {\r\n            \"id\": 48,\r\n            \"quantity\": 1\r\n        }\r\n    ]\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "{{server_url}}api/v1/orders/:id",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"orders",
						":id"
					],
					"variable": [
						{
							"key": "id",
							"value": "2"
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "удаление корзины",
			"request": {
				"method": "DELETE",
				"header": [],
				"url": {
					"raw": "{{server_url}}api/v1/orders/:id",
					"host": [
						"{{server_url}}api"
					],
					"path": [
						"v1",
						"orders",
						":id"
					],
					"variable": [
						{
							"key": "id",
							"value": "2"
						}
					]
				}
			},
			"response": []
		}
	]
}
