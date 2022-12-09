# botimport telegram

# Replace <TOKEN> with the token you received from the BotFather
bot = telegram.Bot(token="<TOKEN>")

# This function will be called every time the bot receives a message
def handle_message(message):
    # Print the message text to the console
    print(message.text)

    # Send the same message back to the user
    bot.send_message(chat_id=message.chat.id, text=message.text)

# Set the bot's message handler
bot.set_message_handler(handle_message)

# Start the bot
bot.start()
