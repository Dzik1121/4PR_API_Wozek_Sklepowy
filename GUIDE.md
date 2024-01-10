# Zapytania

### *Stwórz Konto* 

---
>Aby stworzyć konto, wyślij zapytanie '/api/createUser' używając schematu:
```
{
  "Login": "your_username",
  "Password": "your_password",
  "Email": "your_email@example.com"
}

```
>Powinno zwrócić:
```
{
  "Login": "john_doe",
  "Email": "john.doe@example.com",
  "ID": "some_unique_id",
  "Basket": [],
}

```
### *Logowanie się do Konta*

---
>Aby zalogować się do konta, wyślij zapytanie '/api/loginUser' używając schematu:
```
{
  "Login": "john_doe",
  "Password": "secretpassword"
}
```
>Powinno zwrócić:
```
{
 "Login": "john_doe",
 "Email": "john.doe@example.com",
 "ID": "123456789",
 "Basket": []
}
```
### *Usuwanie Konta*

---
>Aby usunąć konto, wyślij zapytanie '/api/deleteUser' używając schematu:
```

{
  "Login": "john_doe",
  "Email": "john.doe@example.com",
  "ID": "some_unique_id",
  "Basket": [],
}

```
>Powinno zwrócić:
```
{
  "message": "User data deleted successfully"
}

```
### *Dodaj produkt do koszyka*

---

>Aby dodać produkt do koszyka, wyślij zapytanie '/api/addToBasket' używając schematu:
 ```
 {
  "Login": "john_doe",
  "Email": "john.doe@example.com",
  "ID": "some_unique_id",
  "Basket": [],
  "Product_id": "cpu123"
}
 ```
### *Usuń produkt z koszyka*

---

>Aby usunąć produkt z koszyka, wyślij zapytanie '/api/removeBaskets' używając schematu, gdzie 'ProductId' jest Id produktu, który chcemy usunąć:
```
{
  "Login": "example_user",
  "Password": "example_password",
  "Email": "example@example.com",
  "ID": "123456789",
  "Basket": [
    {
      "ProductID": "product_1",
      "ProductName": "Example Product 1",
      "Price": 19.99
    },
    {
      "ProductID": "product_2",
      "ProductName": "Example Product 2",
      "Price": 29.99
    }
  ],
  "ProductId": "product_1"
}

```

### *Wyświetl produkty*


---

>Aby wyświetlić produkty, wyślij zapytanie z GET '/api/getProducts'. Powinno zwrócić:
```
[
  {
    "ID": 1,
    "Name": "Product A",
    "Price": 29.99,
  },
  {
    "ID": 2,
    "Name": "Product B",
    "Price": 49.99,
  },
  {
    "ID": 3,
    "Name": "Product C",
    "Price": 19.99,
  }
]

```
