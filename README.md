# ==========================================
# SOL PLAATJE UNIVERSITY APS CALCULATOR
# Created by: Nontando Fumba
# ==========================================


# FUNCTIONS


def get_mark(subject):
    while True:
        mark = int(input(f"Enter {subject} mark: "))
        if 0 <= mark <= 100:
            return mark
        print("Invalid mark. Marks must be between 0 and 100.")


def mark(score):
    if score >= 90:
        return 8
    elif score >= 80:
        return 7
    elif score >= 70:
        return 6
    elif score >= 60:
        return 5
    elif score >= 50:
        return 4
    elif score >= 40:
        return 3
    elif score >= 30:
        return 2
    else:
        return 1



# SUBJECT MENU 

def choose_home_language():
    print("\nChoose your Home Language")
    print("1. English")
    print("2. isiXhosa")
    print("3. Afrikaans")
    print("4. Sesotho")
    print("5. Setswana")

    choice = input("Choice: ")

    if choice == "1":
        return "English Home Language"
    elif choice == "2":
        return "isiXhosa Home Language"
    elif choice == "3":
        return "Afrikaans Home Language"
    elif choice == "4":
        return "Sesotho Home Language"
    else:
        return "Setswana Home Language"


def choose_other_language():
    print("\nChoose your First Additional Language")
    print("1. English")
    print("2. Afrikaans")
    print("3. isiXhosa")

    choice = input("Choice: ")

    if choice == "1":
        return "English First Additional Language"
    elif choice == "2":
        return "Afrikaans First Additional Language"
    else:
        return "isiXhosa First Additional Language"


def choose_maths():
    print("\nChoose Mathematics")
    print("1. Mathematics")
    print("2. Mathematical Literacy")

    choice = input("Choice: ")

    if choice == "1":
        return "Mathematics"
    else:
        return "Mathematical Literacy"


def choose_science():
    print("\nChoose a Science Subject")
    print("1. Physical Sciences")
    print("2. Life Sciences")
    print("3. Agricultural Sciences")

    choice = input("Choice: ")

    if choice == "1":
        return "Physical Sciences"
    elif choice == "2":
        return "Life Sciences"
    else:
        return "Agricultural Sciences"


def choose_commerce():
    print("\nChoose a Commerce Subject")
    print("1. Accounting")
    print("2. Business Studies")
    print("3. Economics")

    choice = input("Choice: ")

    if choice == "1":
        return "Accounting"
    elif choice == "2":
        return "Business Studies"
    else:
        return "Economics"


def choose_humanities():
    print("\nChoose a Humanities Subject")
    print("1. Geography")
    print("2. History")
    print("3. Tourism")

    choice = input("Choice: ")

    if choice == "1":
        return "Geography"
    elif choice == "2":
        return "History"
    else:
        return "Tourism"



# STUDENT INFORMATION

print("========================================")
print(" SOL PLAATJE UNIVERSITY APS CALCULATOR ")
print("========================================")

name = input("Enter your full name: ")

home_language = choose_home_language()
other_language = choose_other_language()
maths = choose_maths()
science = choose_science()
commerce = choose_commerce()
humanities = choose_humanities()

home_mark = get_mark(home_language)
other_mark = get_mark(other_language)
maths_mark = get_mark(maths)
science_mark = get_mark(science)
commerce_mark = get_mark(commerce)
humanities_mark = get_mark(humanities)
life_orientation = get_mark(life orientation)


# APS CALCULATION


home_aps = mark(home_mark)
other_aps = mark(other_mark)
maths_aps = mark(maths_mark)
science_aps = mark(science_mark)
commerce_aps = mark(commerce_mark)
humanities_aps = mark(humanities_mark)

if life_orientation >= 90:
    lo_aps = 4
elif life_orientation >= 80:
    lo_aps = 3
elif life_orientation >= 70:
    lo_aps = 2
elif life_orientation >= 60:
    lo_aps = 1
else:
    lo_aps = 0

total_aps = (
    home_aps +
    other_aps +
    maths_aps +
    science_aps +
    commerce_aps +
    humanities_aps +
    lo_aps
)

print("\nYour APS is:", total_aps)



# COURSE DATABASE


education = {}

science_courses = {}

commerce_courses = {}

humanities_courses = {}

ict_courses = {}

courses = {}

courses.update(education)
courses.update(science_courses)
courses.update(commerce_courses)
courses.update(humanities_course)
courses.update(ict_courses)

#Qualified Courses 

courses = {
    "BEd Foundation Phase":{
      "aps":30,
      "english":50,
      "other language":50,
      "maths": 40,
      "maths lit ":50
    },
     
     "BEd Intermediate Phase - Maths, Natural Science and Languages":{
        "aps":30,
        "other language":50,
        "maths":50,
        "physical sciences":50,
        "life sciences":50
    },

     "BEd Intermediate Phase - Language, Life skills and Social Sciences":{
        "aps":30,
        "geography":50,
        "history":50
    },

    "BEd Senior Phase - Mathematics and Physical Sciences": {©> 
        "aps": 32,
        "maths": 60,
        "physical sciences": 60,
        "english": 50
    },

    "BEd Senior Phase - English and History": {
        "aps": 30,
        "english": 60,
        "history": 55
    },

    "BEd Senior Phase - Accounting and Business Studies": {
        "aps": 30,
        "Accounting": 60,
        "Business Studies": 55
    },

    "Higher Certificate in Heritage": {
        "aps": 25,
        "english": 50,
        "maths": 30
    },

    "Higher Certificate in Interpreting": {
        "aps": 25,
        "english": 50,
        "other_language": 50
    },

    "Bachelor of Arts": {
        "aps": 30,
        "english": 50,
        "maths": 30,
        "geography": 50
    },

    "Diploma in Agriculture": {
        "aps": 25,
        "english": 50,
        "life_sciences": 40,
        "agricultural_sciences": 40,
        "physical_sciences": 40,
        "maths": 40
    },

    "Diploma in Information and Communication Technology": {
        "aps": 25,
        "english": 50,
        "maths": 40
    },

    "Bachelor of Environmental Science": {
        "aps": 30,
        "physics": 50,
        "maths": 50,
        "english": 50
    },

    "Bachelor of Science": {
        "aps": 30,
        "english": 50,
        "maths": 50,
        "life_sciences": 50
    },

    "Bachelor of Science in Data Science": {
        "aps": 30,
        "english": 50,
        "maths": 60
    },

    "Higher Certificate in Entrepreneurship": {
        "aps": 25,
        "english": 50,
        "maths": 40,
        "accounting": 40,
        "business_studies": 40,
        "economics": 40
    },

    "Diploma in Retail Business Management": {
        "aps": 25,
        "english": 50,
        "maths": 40,
        "accounting": 40,
        "business_studies": 40,
        "economics": 40
    },

    "Bachelor of Commerce": {
        "aps": 30,
        "english": 50,
        "maths": 60,
        "accounting": 40,
    }
}
qualified_courses = []

for course, requirements in courses.items():

    if total_aps >= requirements["aps"]:
        qualified_courses.append(course)

if qualified_courses:
    print("\nCongratulations!")
    print("You qualify for:")

    for course in qualified_courses:
        print("-", course)

else:
    print("Unfortunately you do not qualify for any courses.")
