<h1 align="center">TV Sushi - Product Data</h1>

<p align="center">
  JSON data source for the <a href="https://github.com/AndresBol/TV_Sushi">TV Sushi</a> restaurant website.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Format-JSON-yellow?logo=json&logoColor=white" alt="JSON"/>
  <img src="https://img.shields.io/badge/Served%20via-GitHub%20Raw-black?logo=github&logoColor=white" alt="GitHub Raw"/>
  <img src="https://img.shields.io/badge/Products-10%20items-green" alt="Products"/>
</p>

---

## Purpose

This repository hosts the **product catalog data** consumed by the [TV Sushi](https://github.com/AndresBol/TV_Sushi) frontend website. By externalizing the menu data into a separate repository, the product catalog can be updated independently without modifying or redeploying the main site.

The main website fetches this data at runtime via the GitHub Raw Content API:

```
https://raw.githubusercontent.com/AndresBol/TV_Sushi_Data/main/products.json
```

## Data Schema

The file `products.json` contains an array of product objects with the following structure:

| Field          | Type   | Description                                     |
| -------------- | ------ | ----------------------------------------------- |
| `ID`           | number | Unique product identifier                       |
| `Nombre`       | string | Product name                                    |
| `Descripción`  | string | Product description                             |
| `Ingredientes` | string | Comma-separated list of ingredients             |
| `Precio`       | string | Price in Costa Rican colones (e.g. `"₡ 7 800"`) |
| `Porcion`      | string | Portion size (e.g. `"10 piezas"`, `"1 tazón"`)  |
| `Ruta`         | string | Relative image path used by the main site       |

### Example

```json
{
  "ID": 1,
  "Nombre": "Camarón tempura Roll",
  "Descripción": "Crujientes camarones tempura jumbo envueltos con surimi y suave queso crema.",
  "Ingredientes": "Camarones tempura jumbo, surimi y queso crema",
  "Precio": "₡ 7 800",
  "Porcion": "10 piezas",
  "Ruta": "media/ProductImages/Meal_1.png"
}
```

## Related Repository

| Repository                                        | Description                                                |
| ------------------------------------------------- | ---------------------------------------------------------- |
| [TV_Sushi](https://github.com/AndresBol/TV_Sushi) | Main frontend website - HTML, CSS, JavaScript, Bootstrap 5 |

---

<p align="center">
  <sub>Data repository for the TV Sushi academic project - Universidad Técnica Nacional (UTN)</sub>
</p>
