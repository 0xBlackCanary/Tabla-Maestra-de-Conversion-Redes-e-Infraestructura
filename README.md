# 🔢 Network Architecture & Subnetting Toolkit

> "La automatización y el cálculo preciso de subredes son las bases para auditar la segmentación y el perímetro de cualquier infraestructura."

Este repositorio contiene una guía de referencia rápida para el cálculo de direccionamiento IPv4, conversión de sistemas numéricos (Binario, Decimal, Hexadecimal) y segmentación CIDR, diseñada para agilizar el análisis de paquetes y auditorías de red.

---

## 🎛️ Herramienta Interactiva

Para facilitar las operaciones en tiempo real, he desarrollado una calculadora interactiva con interfaz Cyberpunk integrada directamente en este repositorio.

🚀 **[ACCEDER A LA CALCULADORA INTERACTIVA EN VIVO](https://0xblackcanary.github.io/Tabla-Maestra-de-Conversion-Redes-e-Infraestructura/)**

---

## 🔺 1. Tabla de Equivalencia Hexadecimal (0 - 15)
Guía rápida para traducir cuartetos de bits a un único carácter hexadecimal, fundamental para análisis en Wireshark e infraestructura IPv6.

| Decimal | Binario (4 Bits) | Hexadecimal |
| :---: | :---: | :---: |
| **0** | `0000` | `0` |
| **1** | `0001` | `1` |
| **2** | `0010` | `2` |
| **3** | `0011` | `3` |
| **4** | `0100` | `4` |
| **5** | `0101` | `5` |
| **6** | `0110` | `6` |
| **7** | `0111` | `7` |
| **8** | `1000` | `8` |
| **9** | `1001` | `9` |
| **10** | `1010` | `A` |
| **11** | `1011` | `B` |
| **12** | `1100` | `C` |
| **13** | `1101` | `D` |
| **14** | `1110` | `E` |
| **15** | `1111` | `F` |

---

## 🌐 2. Análisis del CIDR de un Vistazo (/24 vs /26)
Entendiendo la asignación de bits de red frente a los bits de host para evaluar la segmentación interna.

### ▪️ El Bloque Base: `/24`
* **Máscara Decimal:** `255.255.255.0`
* **Estructura de Bits:** `11111111.11111111.11111111.00000000`
* **Capacidad:** 1 única red plana con **254 hosts direccionables** (del `.1` al `.254`).

### ▪️ La Segmentación Avanzada: `/26`
* **Máscara Decimal:** `255.255.255.192`
* **Estructura de Bits:** `11111111.11111111.11111111.11000000`
* **Capacidad:** Divide el bloque original en **4 subredes independientes** de **62 hosts útiles** cada una:

| Subred | Dirección de Red | Rango de IPs Útiles | Dirección de Broadcast |
| :---: | :---: | :---: | :---: |
| **#1** | `.0` | `.1` - `.62` | `.63` |
| **#2** | `.64` | `.65` - `.126` | `.127` |
| **#3** | `.128` | `.129` - `.190` | `.191` |
| **#4** | `.192` | `.193` - `.254` | `.255` |

---

## 🛠️ Despliegue Técnico
El panel interactivo está construido utilizando **HTML5, CSS3 nativo con variables personalizadas para el entorno neón, y lógica de cálculo en JavaScript síncrono**. No requiere dependencias externas ni backend, garantizando un entorno ligero y portable.

