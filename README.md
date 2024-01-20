# Sample-Python-code-using-flask-framework-for-creating-Resume-in-Webpage
#This is a sample Python code with flask framework for creating Resume in Webpage. The Python script contains html tag too
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    resume_data = {
        "name": "Mohana Priya.T",
        "email": "mohana192k@gmail.com",
        "linkedin_url": "https://www.linkedin.com/in/mohana-priya-t-122385182",
        "dob": "19-03-2000",
        "instruction": "Click on the below headers to get the respective information",
        "career_objective": """Results-driven Scientific Application Analyst with 2.3 years of experience in configuring 
                                ELN (Electronic Laboratory Notebooks) for R&D scientists, utilizing SQL and Database
                                expertise. Seeking a challenging role in an organization to leverage my technical skills, spatial 
                                thinking, and optimization abilities to contribute to the organization's growth while expanding 
                                my knowledge.""",
        "work_experience": """
                            <ul>
                                <li>Scientific Application Analyst - Zifo RnD Solutions (Dec 2021 - Dec 2022)
                                    <ul>
                                        <li>Created a proof of concept (POC) for a Waterfall project using an ELN and 
                                        successfully obtained client approval.</li>
                                        <li>Conducted requirements analysis and breakdown for complex tasks, ensuring a 
                                        clear understanding of project objectives and deliverables.</li>
                                        <li>Prepared timelines and estimates for projects, effectively managing project 
                                        schedules and resources.</li>
                                        <li>Demonstrated expertise in training individuals in product-based trainings for 
                                        Dotmatics, providing comprehensive guidance and mentoring.</li>
                                        <li>Presented project work to customers through engaging demos, effectively 
                                        showcasing project features and benefits.</li>
                                        <li>Managed email correspondence efficiently, ensuring effective communication
                                        and timely responses.</li>
                                        <li>Provided technical support, incident management and system maintenance for 
                                        an ELN tool.</li>
                                    </ul>
                                </li>
                                <li>Associate Analyst - Zifo RnD Solutions (Dec 2020 - Dec 2021)
                                    <ul>
                                        <li>Played a dual role as a developer and tester for an ELN tool within an Agile 
                                        project environment.</li>
                                        <li>Collaborated closely with foreign customers, gaining valuable exposure to 
                                        international work dynamics and fostering effective cross-cultural 
                                        communication.</li>
                                        <li>Acquired knowledge and hands-on experience with Scrum methodologies and 
                                        collaboration tools such as Azure and JIRA board, contributing to efficient project 
                                        management and teamwork.</li>
                                        <li>Created training and testing documents, including user-friendly training videos, to 
                                        facilitate user understanding of the ELN tool's functionality and usage.</li>
                                        <li>Utilized UML and Visual Studio tools to develop flowcharts and workflow 
                                        models, enhancing comprehension and visualization of system processes.</li>
                                        <li>Demonstrated proficiency in writing test scripts and executing test cases, 
                                        ensuring comprehensive testing coverage and high software quality.</li>
                                    </ul>
                                </li>
                                <li>Associate Analyst Intern - Zifo RnD Solutions (Aug 2020 - Nov 2020)
                                    <ul>
                                        <li>Trained in SQL based ELN.</li>
                                    </ul>
                                </li>
                            </ul>
                            """,
        "academics": """<li> Completed B.Sc. Mathematics with Computer Applications at Dr. N.G.P. Arts and 
                        Science college with an aggregate of 88%(2017-2020)</li>""",
        "projects": """<ul>1. Endotoxin Protocol
                            <ul>
                            <li>Designed and configured the Endotoxin testing protocol using ELN functionalities, 
                            ensuring accurate and efficient data capture and analysis.</li>
                            <li>Utilized SQL coding to implement the necessary configurations, ensuring seamless 
                            integration with the existing systems.</li>
                            <li>Employed UML tool and Azure DevOps for writing comprehensive test scripts, ensuring 
                            thorough testing coverage and efficient execution.</li>
                            <li>Collaborated with cross-functional teams to facilitate integration using API calls and 
                            Python scripts, enabling data exchange between different systems.</li>
                            <li>Led the successful migration of the project from the development environment to the 
                            production environment, ensuring minimal disruption and smooth transition.</li>
                            </ul> 
                        2. Parallel Synthesis Workflow Protocol
                            <ul>
                            <li>Enhanced the Synthesis workflow that is already configured by Dotmatics team using additional 
                            Dotmatics modules and SQL tuning. Involved in Server installation that includes Tomcat, DB 
                            and Dotmatics upgradation.</li>
                            </ul>
                        3. NanoString Protocol
                            <ul>
                            <li>Configured protocol for obtaining data from an instrument using Python script and displaying 
                            it in Dotmatics. This includes custom data Visualization.</li>
                        </ul>
                            
                            </ul>""",
        "additional_qualifications": """<li>Python certificate of completion by IIT - Madras using GUVI support (06/2023)</li>
                                        <li>Completed Advanced SQL: SQL Expert Certification Preparation course from Udemy 
                                        (06/2022)</li>
                                        <li>Become a Data Scientist course from LinkedIn learning (08/2022)</li>""",
        "technical_skills": """<li>SQL - Advanced</li>
                            <li>Python - Intermediate</li> 
                            <li>Microsoft Office – Word, Excel, Power point</li>
                            <li>Mongo DB, NoSQL, Power Bi, Tableau - Beginner</li>
                            <li>Testing knowledge and Documentation</li>""",
        "area_of_interest": """<li>Analytics</li>
                            <li>SQL Developer</li> 
                            <li>Support and Testing""",
        "personal_attributes": """<li>Inductive reasoning</li>
                                <li>Customer handling</li> 
                                <li>Critical thinking and flexible</li> 
                                <li>Capable to shoulder any responsibility</li>""",
        "volunteer_activities": """<li>A Creative thinking volunteer to the Team Everest NGO (06/2021 - 07/2021)</li>""",
        "language": """<li>English - Fluent</li> 
                    <li>Tamil - Native</li>"""
    }

    html_content = f"""
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>{resume_data['name']}</title>
        <style>
            .section {{
                display: none;
            }}
        </style>
        <script>
            function toggleSection(sectionId) {{
                var section = document.getElementById(sectionId);
                if (window.getComputedStyle(section).display === 'none') {{
                    section.style.display = 'block';
                }} else {{
                    section.style.display = 'none';
                }}
            }}
        </script>
    </head>
    <body>
        <h1>{resume_data['name']}</h1>
        <p><strong>Email:</strong> {resume_data['email']}</p>
        <p><strong>LinkedIn:</strong> <a href="{resume_data['linkedin_url']}" target="_blank">{resume_data['linkedin_url']}</a></p>
        <p><strong>DOB:</strong> {resume_data['dob']}</p>
        <p style="color: #3366cc;"><strong>{resume_data['instruction']}</strong></p>

        <h2 onclick="toggleSection('careerObjective')">Career Objective</h2>
        <div class="section" id="careerObjective">
            <p>{resume_data['career_objective']}</p>
        </div>

        <h2 onclick="toggleSection('workExperience')">Work Experience</h2>
        <div class="section" id="workExperience">
            <p>{resume_data['work_experience']}</p>
        </div>

        <h2 onclick="toggleSection('academics')">Academics</h2>
        <div class="section" id="academics">
            <p>{resume_data['academics']}</p>
        </div>

        <h2 onclick="toggleSection('projects')">Projects</h2>
        <div class="section" id="projects">
            <p>{resume_data['projects']}</p>
        </div>

        <h2 onclick="toggleSection('additional_qualifications')">Additional Qualifications</h2>
        <div class="section" id="additional_qualifications">
            <p>{resume_data['additional_qualifications']}</p>
        </div>

        <h2 onclick="toggleSection('technical_skills')">Technical Skills</h2>
        <div class="section" id="technical_skills">
            <p>{resume_data['technical_skills']}</p>
        </div>

        <h2 onclick="toggleSection('area_of_interest')">Area of Interest</h2>
        <div class="section" id="area_of_interest">
            <p>{resume_data['area_of_interest']}</p>
        </div>
        
        <h2 onclick="toggleSection('personal_attributes')">Personal Attributes</h2>
        <div class="section" id="personal_attributes">
            <p>{resume_data['personal_attributes']}</p>
        </div>

        <h2 onclick="toggleSection('volunteer_activities')">Volunteer Activities</h2>
        <div class="section" id="volunteer_activities">
            <p>{resume_data['volunteer_activities']}</p>
        </div>

        <h2 onclick="toggleSection('language')">Language</h2>
        <div class="section" id="language">
            <p>{resume_data['language']}</p>
        </div>
    </body>
    </html>
    """

    return html_content

if __name__ == '__main__':
    app.run(debug=True)

