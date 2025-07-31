```python
class Read_Me:
    def __init__(self, username = "mvinza34", year = 2025):
        self.year = year
        self.username = username
        self.intro = {
            'introduction': ['Marlon Vinza', '26-year-old', 'college graduate']
        }
        self.education = {
            'engineering': ['Computer Engineering', 'Sacred Heart University', 'Bachelor of Science']
        }
        self.employment = {
            'engineer': ['companies', 'city'],
            'volunteer': ['Note-Taker', 'Freshman Seminar']
        }
        self.skills = { 
            'programming languages': ['Python', 'MATLAB', 'SystemVerilog'],
            'software': ['Visual Studio', 'Microsoft Office'],
            'hardware': ['Raspberry Pi 4', 'Raspberry Pi Pico', 'Arduino Uno'] 
        }
        self.growing = {
            'programming languages': ['Ladder Logic', 'Structured Text'],
            'software': ['TIA Portal'],
            'hardware': [],
            'learning sites': ['YouTube']
        }
        self.hobbies = {
            'video games': ['Elden Ring', 'Ghost of Tsushima', 'Dark Souls', 'Lies of P', 'Super Mario Galaxy 2', 'The Witcher 3: Wild Hunt'],
            'books': ['The Lord of the Rings', 'Ultimate Spider-Man', 'A Song of Ice and Fire', 'The Witcher'],
            'movies': ['Godzilla Minus One', 'Avengers: Endgame', 'Star Wars: Return of the Jedi', 'The Lord of the Rings: The Two Towers', 'Spider-Man 2'],
            'TV shows': ['Dragon Ball Z', 'Game of Thrones', 'Code Geass', 'House of the Dragon']
        }
 
    def doing(self, now = 2025):
        today = self.year
        if now < today:
            education = self.education['engineering']
            experience = self.employment['volunteer']
            intro = self.intro['introduction']
            return  """
            Hello there. My name is {name}, and I am a {age} {status}.
            """.format(name = intro[0], age = intro[1], status = intro[2]) + """
            I studied {major} at {university} from 2017 to 2021, obtaining a {degree} degree upon graduation.
            """.format(major = education[0], university = education[1], degree = education[2]) + """
            During my junior year, I volunteered as a {position} for a class called {course}.
            I documented and uploaded comprehensive lecture notes and revised presentations to an online portal.
            This provided students with ongoing access to study materials and enhanced their understanding of the course content.
            """.format(position = experience[0], course = experience[1])

        elif now == today:
            dream = self.growing['programming languages']
            learn_1 = self.growing['software']
            learn_2 = self.growing['learning sites']
            hobby_1 = self.hobbies['video games']
            hobby_2 = self.hobbies['books']
            hobby_3 = self.hobbies['movies']
            hobby_4 = self.hobbies['TV shows']
            return """
            I am currently learning {code_1} and {code_2} via {source}, using {website} as a source.
            """.format(code_1 = dream[0], code_2 = dream[1], source = learn_1[0], website = learn_2[0]) + """
            My hobbies are playing video games, reading books, and watching movies and TV shows. 
            My all-time favorites are {game}, {book}, {movie}, and {show} respectively.
            """.format(game = hobby_1[0], book = hobby_2[1], movie = hobby_3[2], show = hobby_4[2])

        elif now > today:
            goal = self.employment['engineer']
            return """
            I am eager to collaborate with {teams} on {projects}.
            """.format(teams = goal[0], projects = 'software engineering, automation, and electronics')
        else:
            return """
            ### Hi there 👋
            """
        
    def collaborate(self, role, organization, location):
        opportunity = self.employment
        opportunity[role] = [organization, location]

past_me = Read_Me(2025)
present_me = Read_Me(2025)
future_me = Read_Me(2025)

print(past_me.doing(2024))
print(present_me.doing(2025))
print(future_me.doing(2026))
