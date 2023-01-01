```python
class Read_Me:
    def __init__(self, username = "mvinza34", year = 2023):
        self.year = year
        self.username = username
        self.intro = {
            'introduction': ['Marlon Vinza', '23-year-old', 'college graduate']
        }
        self.education = {
            'engineering': ['Computer Engineering', 'Sacred Heart University', 'Bachelor of Science']
        }
        self.employment = {
            'engineer': ['company', 'city'],
            'volunteer': ['Note-Taker', 'Freshman Seminar']
        }
        self.skills = { 
            'programming languages': ['Python', 'Arduino', 'MATLAB', 'SystemVerilog'],
            'software': ['Microsoft Office'],
            'hardware': ['Arduino Uno'] 
        }
        self.growing = {
            'programming languages': ['C#'],
            'software': ['Visual Studio'],
            'hardware': ['Raspberry Pi','Raspberry Pi Pico'],
            'learning sites': ['YouTube', 'freeCodeCamp', 'Code Academy']
        }
        self.hobbies = {
            'video games': ['Elden Ring', 'Ghost of Tsushima', 'The Witcher 3: Wild Hunt', 'The Legend of Zelda: Breath of the Wild'],
            'books': ['The Lord of the Rings', 'A Song of Ice and Fire', 'The Witcher'],
            'movies': ['Avengers: Endgame', 'The Lord of the Rings: The Two Towers', 'Spider-Man 2'],
            'tv shows': ['Dragon Ball', 'Game of Thrones', 'Code Geass', 'House of the Dragon']
        }
 
    def doing(self, now = 2023):
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
            I guided special needs students by documenting notes for them 
            and revised and clarified presentation content when needed.
            """.format(position = experience[0], course = experience[1])

        elif now == today:
            dream = self.growing['programming languages']
            learn = self.growing['learning sites']
            hobby_1 = self.hobbies['video games']
            hobby_2 = self.hobbies['books']
            hobby_3 = self.hobbies['movies']
            hobby_4 = self.hobbies['tv shows']
            return """
            I am currently learning {code} on {website} and {other}.
            """.format(code = dream[0], website = learn[0], other = learn[2]) + """
            My hobbies are mainly playing video games, reading books, and watching movies and tv shows. 
            My all time favorites are {game}, {book}, {movie}, and {show} respectively.
            """.format(game = hobby_1[0], book = hobby_2[1], movie = hobby_3[2], show = hobby_4[2])

        elif now > today:
            goal= self.employment['engineer']
            return """
            I am eager to collaborate with {teams} on {projects}.
            """.format(teams = goal[0], projects = 'software engineering and electronics')
        else:
            return """
            ### Hi there 👋
            """
        
    def collaborate(self, role, organization, location):
        opportunity = self.employment
        opportunity[role] = [organization, location]

past_me = Read_Me(2023)
present_me = Read_Me(2023)
future_me = Read_Me(2023)

print(past_me.doing(2022))
print(present_me.doing(2023))
print(future_me.doing(2024))
