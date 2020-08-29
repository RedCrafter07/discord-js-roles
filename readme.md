# discord-js-roles
Rollen-Verwaltung in discord.js
Dies ist ein kleiner Walkthrough durch alle Rollen.

> ## Rolle erstellen
> Rollen werden grundsätzlich mit dem Guild verknüpft. Dies tut man mit message.guild.
>
> ### Code
> ```javascript
> message.guild.roles.create({
>    data:   {
>        name: 'NAME DER ROLLE',
>        color: 'FARBE'
>   }
> })
> ```

> ## Rolle nach Name suchen
> Das nächste wäre, die Rolle nach dem Namen zu suchen. Das tut man so:
> ```javascript
> const role = message.guild.roles.cache.find((role) => role.name === 'ROLLEN NAME');
> ```

> ## Rolle in Permissions (für Kanäle etc.) anwenden
> Man benutzt den Code von oben und überschreibt die Permissions mit einer ID