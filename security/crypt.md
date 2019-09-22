Рекомендации по шифрованию информации
===

### Общие рекомендации

* ипользуйте проверенные временем алгоритмы шифрования
* не изобретайте велосипедов
* для более стойкого шифрования данных, можно сочетать несколько алгоритмов, например, `RSA` + `AES`
* ипользуйте соль
* используйте случайные ключи

### Используем AES

	шифрованные данные = AES(IV, text + salt).
	
`IV` каждый раз генерить новый, передавать вместе с шифром.
`Salt` каждый раз генерить новый, передавать только длину, саму соль передавать нежелательно.
На принимающей стороне соль можно просто вырезать, зная положение и длину.

* Используйте AES-256 в режиме CTR со случайным одноразовым кодом