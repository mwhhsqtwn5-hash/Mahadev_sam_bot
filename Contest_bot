bot.py
from telegram import Update, ReplyKeyboardMarkup
from telegram.ext import Updater, CommandHandler, MessageHandler, Filters, CallbackContext

BOT_TOKEN = AAFZ3s IP-3X
LnsX8aKeР3NТХig6EDZеMbE

def start(update: Update, context: CallbackContext):
    keyboard = [
        ["💰 Wallet", "📋 Available Contests"],
        ["➕ Deposit", "➖ Withdraw"]
    ]
    update.message.reply_text(
        "Welcome to Fantasy Contest Bot",
        reply_markup=ReplyKeyboardMarkup(keyboard, resize_keyboard=True)
    )

def handle_message(update: Update, context: CallbackContext):
    text = update.message.text

    if text == "💰 Wallet":
        update.message.reply_text("Wallet Balance: ₹0")

    elif text == "📋 Available Contests":
        update.message.reply_text(
            "IND vs AUS\nEntry ₹49\nPrize ₹5000"
        )

    elif text == "➕ Deposit":
        update.message.reply_text("UPI payment karke UTR bhejo")

    elif text == "➖ Withdraw":
        update.message.reply_text("UPI ID aur amount bhejo")

def main():
    updater = Updater(BOT_TOKEN)
    dp = updater.dispatcher
    dp.add_handler(CommandHandler("start", start))
    dp.add_handler(MessageHandler(Filters.text & ~Filters.command, handle_message))
    updater.start_polling()
    updater.idle()

main()
