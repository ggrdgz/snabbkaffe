# snabbkaffe
An easy to use [Hugo](https://gohugo.io/) theme for a café or coffee shop.

## Important
You need to have a `content/_index.md` file.

## Configuration
```yaml
# hugo.yaml

locale: en-US
title: <h1_for_site>
params:
  company: <company_name>
  currency: USD
  precision: 2
  footerTagLine: "E.g.: The best coffee in town etc."
  description: <meta_description>
  openGraph:
    image:
      url: /images/foo.jpg
      alt: alt text
```

### Intro
```yaml
# data/intro.yaml

title: About Us
content: >
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras diam dolor,
  elementum quis nulla ut, condimentum condimentum metus. Nam quis nisl
  sollicitudin, sodales sem at, molestie felis. Nunc ut dolor magna. Sed
  ornare felis sed nisi convallis varius. Vivamus ex nisl, suscipit
  consequat ipsum non, pharetra tristique elit.
image:
  url: /images/intro.jpg
  alt: alt text
```

### Menu
```yaml
# data/menu/image.yaml

url: /images/menu.jpg
alt: menu etc.
```
Key `weight` decides the order of appearance in the `menu` section.
```yaml
# data/menu/coffee.yaml

title: Coffee and drinks
weight: 1
items:
  - name: Espresso
    description: Rich Italian espresso.
    price: 5

  - name: Cappuccino
    description: Espresso with steamed milk and milk foam.
    price: 10
    addons:
      - name: Extra espresso shot
        price: 5
      - name: Oat milk
        price: 5
      - name: Vanilla syrup
        price: 5

  - name: Latte
    description: Espresso with plenty of steamed milk.
    price: 10

  - name: Tea
    price: 5
```
```yaml
# data/menu/food.yaml

title: Food
weight: 2
items:
  - name: Grilled Sandwich
    description: Grilled sandwich with cheese and ham.
    price: 20
    addons:
      - name: Extra cheese
        price: 5
      - name: Bacon
        price: 5
  - name: Caesar Salad
    description: Chicken, parmesan, croutons and Caesar dressing.
    price: 25
  - name: Soup of the Day
    price: 15
```

### Opening hours
```yaml
# data/openingHours.yaml

title: Opening Hours
schedule:
  - days: Monday - Friday
    from: '07:30'
    to: '18:00'
  - days: Saturday
    from: '09:00'
    to: '18:00'
  - days: Sunday
    from: '10:00'
    to: '18:00'
image:
  url: /images/open.jpg
  alt: alt text
```

### Location
```yaml
# data/location.yaml

title: Location
address:
  street: <street>
  postalCode: <postal_code>
  city: <city>
  country: <country>
```

### Contact
```yaml
# data/contact.yaml

title: Contact Us
phone:
  label: Telephone
  number: <telephone_number>
  displayNumber: <display_format>
mail:
  label: E-mail
  address: <email_address>
```

