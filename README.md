# Livolo Home Assistant Integration

Home Assistant custom component Livolo okoskapcsolók és dimmerek vezérlésére, Livolo Gateway-en keresztül, felhős kapcsolattal.

## Funkciók

- Kapcsolók és dimmerek vezérlése Home Assistantból
- Valós idejű frissítés MQTT-n keresztül
- Automatikus eszközfelismerés
- Többcsatornás kapcsolók támogatása (PowerSwitch_1, PowerSwitch_2, stb.)
- **Dimmer támogatás** (Dimming_panel kategória, fényerő szabályozással)

## Telepítés HACS-szal

1. Telepítsd a [HACS](https://hacs.xyz/)-t
2. HACS → Integrations → Custom repositories
3. Repo URL: `https://github.com/kristof-farkas/livolo_home_assistant`
4. Típus: Integration → Add
5. Keresd meg a "Livolo" integrációt és telepítsd
6. Indítsd újra a Home Assistantot
7. Settings → Devices & Services → Add Integration → "Livolo"

## Konfiguráció

Beállításkor szükséges adatok:
- **Email** és **Password**: Livolo fiók adatok
- **Country Code**: pl. `DE`, `US`, `CN`
- **APP Key** és **APP Secret**: az [APK-ból kinyerhető](https://www.javadecompilers.com/apk) (`appKey` és `appSecret` mezők), vagy az [SDKInitHelper.java](https://github.com/PengJiang520/livoloapp) fájlból

## Követelmények

- Home Assistant 2024.1.0+
- paho-mqtt>=1.6.1
- aiohttp>=3.9.0
- cryptography>=41.0.0

## Hibaelhárítás

- **Eszközök nem jelennek meg**: ellenőrizd a bejelentkezési adatokat és a HA logokat
- **Nincs valós idejű frissítés**: ellenőrizd az MQTT kapcsolatot a logokban (port 1883)

## ⚠️ Figyelmeztetés

Ez egy nem hivatalos, beta integráció, nincs kapcsolatban a Livolo céggel. A Livolo felhőszolgáltatás változásai bármikor megszakíthatják a működést. Saját felelősségre használd.
