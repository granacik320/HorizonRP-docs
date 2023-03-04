---
sidebar_position: 3
---

# Dispatch
Skrypt do wyświetlania powiadomień na dispatchu policji

##Create
-```popupid``` ID powiadomienia
-```title``` Tytuł
-```info``` Informacje, miejsce zdażenia
-```code``` Kod akcji
-```maxcount``` Maksymalna ilość jednostek
-```buttons``` Przyciski ```lokalizacja```, ```reaguj```

```js title="server.lua"
TriggerClientEvent("dispatch:create", -1, popupid, title, info, code, maxcount, buttons)
```

##Update
-```popupid``` ID powiadomienia
-```count``` aktualna liczba jednostek

```js title="server.lua"
TriggerClientEvent("dispatch:update", -1, popupid, count)
```