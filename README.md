import discord

token='MTExNTQyMDE4Nzk5MTIyMDM0Ng.G0R6d4.ddjlGME8FGXzBxKmanTfr5osAUimVeZtPrRhA'
client = discord.bot()


@client.event
async def on_ready():
  print("on_ready")


@client.slash_command()
async def hello(ctx):
  await ctx.respond("こんにちは")


@client.slash.command()
async def name_hello(ctx, name):
  await ctx.respond(name + "さんこんにちは")


client.run(token)
