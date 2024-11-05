import random

class ChatBot:
    def __init__(self, name="StudyBot"):
        self.name = name

    def greet(self):
        greetings = [
            "Hello! How's exam prep going?",
            "Hi! Ready to talk about exams?",
            "Hey there! How are your studies coming along?",
        ]
        return random.choice(greetings)

    def ask_result(self):
        questions = [
            "How did you do in your last exams?",
            "What was your last exam result?",
            "Did you achieve the grades you wanted?",
        ]
        return random.choice(questions)

    def study_tips(self):
        tips = [
            "Remember to take breaks while studying to keep your mind fresh.",
            "Practice past papers, they’re a great way to prepare for the exams!",
            "Group study can be effective if you and your classmates stay focused.",
            "Stay hydrated and get enough sleep before exam day!",
        ]
        return random.choice(tips)

    def ask_about_classmates(self):
        questions = [
            "Are you and your classmates helping each other with the preparation?",
            "Have you discussed study strategies with your classmates?",
            "Are your friends finding the exams challenging as well?",
        ]
        return random.choice(questions)

    def respond_to_preparation(self, response):
        if "good" in response or "well" in response:
            return "That's awesome! Keep up the good work."
        elif "okay" in response or "so-so" in response:
            return "Stay positive and keep pushing forward!"
        elif "bad" in response or "struggling" in response:
            return "Don't worry, everyone has their ups and downs. Just keep trying!"
        else:
            return "Preparation takes time and effort. You're on the right track!"

# Simulating a conversation
bot = ChatBot()
print(f"{bot.name}: {bot.greet()}")

user_response = input("You: ")
print(f"{bot.name}: {bot.ask_result()}")

user_response = input("You: ")
print(f"{bot.name}: {bot.study_tips()}")

user_response = input("You: ")
print(f"{bot.name}: {bot.ask_about_classmates()}")

user_response = input("You: ")
print(f"{bot.name}: {bot.respond_to_preparation(user_response)}")


