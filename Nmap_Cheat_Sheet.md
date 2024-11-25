
# 📜 Nmap Cheat Sheet - Comandos Esenciales

## 🛠️ **Escaneos básicos**
- Escaneo rápido de puertos:
  ```bash
  nmap <IP>
  ```
- Escaneo de un rango de IPs:
  ```bash
  nmap <IP_inicio>-<IP_fin>
  ```
- Escaneo de puertos específicos:
  ```bash
  nmap -p <puerto1,puerto2> <IP>
  ```

## 🔍 **Detección de servicios y versiones**
- Detectar servicios y versiones en puertos abiertos:
  ```bash
  nmap -sV <IP>
  ```
- Escaneo con scripts NSE (estándar):
  ```bash
  nmap -sC <IP>
  ```
- Combinación de scripts NSE y detección de versiones:
  ```bash
  nmap -sC -sV <IP>
  ```

## ⚡ **Optimización de velocidad**
- Forzar un escaneo rápido:
  ```bash
  nmap --min-rate 1000 <IP>
  ```
- Escaneo con menos precisión pero más rápido:
  ```bash
  nmap -T4 <IP>
  ```

## 🔐 **Escaneos sin ping**
- Escaneo para hosts que bloquean ICMP:
  ```bash
  nmap -Pn <IP>
  ```

## 🕵️ **Detección de sistema operativo**
- Identificar el sistema operativo:
  ```bash
  nmap -O <IP>
  ```

## 🚪 **Escaneos de puertos específicos**
- Escaneo de los primeros 1000 puertos:
  ```bash
  nmap <IP>
  ```
- Escaneo de todos los puertos:
  ```bash
  nmap -p- <IP>
  ```

## 🎯 **Escaneos agresivos**
- Obtener toda la información posible (puertos, servicios, OS, scripts NSE):
  ```bash
  nmap -A <IP>
  ```

## 📁 **Exportar resultados**
- Exportar resultados en formato XML:
  ```bash
  nmap -oX resultado.xml <IP>
  ```
- Exportar resultados en todos los formatos (normal, XML, grepable):
  ```bash
  nmap -oA resultado <IP>
  ```

## 📂 **Escaneos en red**
- Escaneo de red completa (subred /24):
  ```bash
  nmap 192.168.1.0/24
  ```
- Escaneo en un rango de IPs:
  ```bash
  nmap 192.168.1.100-120
  ```

## 🚨 **Detección de vulnerabilidades (NSE Scripts)**
- Buscar vulnerabilidades comunes:
  ```bash
  nmap --script vuln <IP>
  ```
- Escanear versiones específicas de servicios para vulnerabilidades:
  ```bash
  nmap --script=ssl-heartbleed <IP>
  ```
- Ejecutar un script NSE específico:
  ```bash
  nmap --script=<script_name> <IP>
  ```

## 💡 **Opciones adicionales**
- Mostrar servicios detectados en detalle:
  ```bash
  nmap -sV --version-intensity 5 <IP>
  ```
- Ver paquetes enviados durante el escaneo:
  ```bash
  nmap --packet-trace <IP>
  ```
