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
> ## Was passiert bei diesem Code?
> Es wird die variable "role" definiert. Diese sucht aus dem Catch des Guilds in dem die Nachricht gesendet wurde. Dies wird in einer Funktion unter "role" gespeichert. Dann wird der Rollenname mit role.name gesucht.