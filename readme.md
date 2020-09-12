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

> ## Rolle nach ID suchen
> Eine Rolle per ID zu suchen ist viel genauer, als es durch den Namen zu machen.
> ```javascript
>   const role = message.guild.roles.cache.get("role-id");
> ```
>

> ## Rolle in Permissions (für Kanäle etc.) anwenden
> Man benutzt den Code von oben und überschreibt die Permissions mit einer ID.
> ```javascript
>   const role = message.guild.roles.cache.get("role-id");
>   channelSelector.overwritePermissions({
>       role.id:    {
>           allow:  ["PERMISSIONS HIER"], //Die Permissions, die er für die Rolle im Kanal erlauben soll. 
>           deny:  ["PERMISSIONS HIER"], //Die Permissions, die er für die Rolle im Kanal verbieten soll. 
>       }
>   })
> ```
> An die, die nicht so gut in JS sind: Jede Permission hat einen String. Mehrere werden mit einem Komma getrennt.
>
> Die Permissions findest du [hier](https://discord.com/developers/docs/topics/permissions)
>
> Ich weiß nicht, ob das alles richtig ist, aber dies wäre ein Rollen-Verwaltungs-Code sein.
> 
> Falls du mehr erfahren möchtest, schaue [hier](https://discordjs.guide/popular-topics/permissions.html#roles-as-bot-permissions) vorbei.