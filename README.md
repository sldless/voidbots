
## Installation
`pip install voidbots -U`

## Documentation
To see the voidbots docs [click here](https://docs.voidbots.net/).

Before using this module, Please view [Ratelimits](https://docs.voidbots.net/#/ratelimits) and [Caching](https://docs.voidbots.net/#/caching).

## Example
```
import voidbots as vd
from discord.ext.commands import Bot

bot = Bot(command_prefix='vd!')

@bot.event
async def on_ready()
    print(f'{bot.user.name} is online!')
    await Void.postStats(bot.user.id, len(bot.guilds), bot.shard_count)
    print(f'{bot.user.name} has been posted to Voidbots')

bot.run('Your bot token')
 #This is just examples , it should work.
```

## Functions
```
Void = vd.VoidClient(bot, apikey='Your api key')
await Void.get_voteinfo('Bot ID','A user id')
await Void.get_botinfo('Bot ID')
await Void.postStats(bot.user.id, len(bot.guilds), bot.shard_count or 0)
await Void.get_analytics(bot.user.id)
await Void.get_reviews(bot.user.id)
await Void.widget(bot.user.id, theme='dark or light')
await Void.get_userinfo("User ID")
await Void.get_pack("Pack ID")
await Void.close() #This has a bot_close arg if that is set to true it will close your bot.
```
