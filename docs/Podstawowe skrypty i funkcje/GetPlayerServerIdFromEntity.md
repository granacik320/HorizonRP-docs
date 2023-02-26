---
sidebar_position: 1
---

# GetPlayerServerIdFromEntity

:::info

Funkcja ta działa tylko po stronie ```client``` i jest napisana w języku **lua**.

:::

Funcja ta pobiera id entity i zamienia go na id gracza.

```js title="client.lua"
function GetPlayerServerIdFromEntityId(data)
 if IsEntityAPed(data.entity) and IsPedAPlayer(data.entity) then
   local target = NetworkGetPlayerIndexFromPed(data.entity)
   local playerServerId = GetPlayerServerId(target)
   return playerServerId
 end
 return nil
end
```