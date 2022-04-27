import discord

intents = discord.Intents(messages=True, typing=True, members=True, reactions=True)


class MyClient(discord.Client):
    async def on_message(self, message):
        if message.author == MyClient.user:
            return

        if message.content.startswith("!fuck"):
            await message.channel.send("haha NO")

        if message.content.startswith("!death"):
            await message.channel.send("`I support`")

        if message.content.startswith("!life"):
            await message.channel.send("you're joking right? I mean life is trash I don't see the point.")

        if message.content.startswith("!lie"):
            await message.channel.send("HMM yes, life's only true certainty, aside from death that is...")

    async def on_message_delete(message):
        await message.channel.send("don't hide shit from me")

    async def on_ready(self):
        print("am done you asshole")

    async def on_typing(self, channel, user, when):
        await channel.send("don't type you idiot")

#    async def on_reaction_add(self, reaction, user):
#        message = reaction.message
#        await message.channel.send(user.mention + "just, don't")


client = MyClient()
client.run("token")

# https://discord.com/api/oauth2/authorize?client_id=968280354446270464&permissions=414464723136&scope=bot
