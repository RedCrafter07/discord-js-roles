# discord-js-roles
Rollen-Verwaltung in discord.js

> ## Rolle erstellen
> Rollen werden grundsätzlich mit dem Guild verknüpft. Wir werden es daher mit dem Guild verknüpfen.
> 
> ```javascript
> 
>   //Standardsetup
>   const Discord = require(discord.js)
>   const client = new Discord.Client()
>   client.on("message", (message) => {
>          
>       if(message.content.startsWith(prefix + "addrole"))  {
>           const rolename = message.content.slice()
>       }
>
>   })
> ```