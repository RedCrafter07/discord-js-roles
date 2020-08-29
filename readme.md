# discord-js-roles
Rollen-Verwaltung in discord.js
Dies ist ein kleiner Walkthrough durch alle Rollen.

> ## Rolle erstellen
> Rollen werden grundsätzlich mit dem Guild verknüpft. Wir werden es daher mit dem Guild verknüpfen.
 
> ## Wie erstelle ich eine Rolle in Discord.js?
> ```javascript
> message.guild.roles.create({
>    data:   {
>        name: 'NAME DER ROLLE',
>        color: 'FARBE'
>   }
> })
> ```