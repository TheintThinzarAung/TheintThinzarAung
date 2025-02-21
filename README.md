# generate_chart.py
import matplotlib.pyplot as plt

# Define skills and proficiency percentages
skills = ['Python', 'SQL', 'ML', 'Data Viz']
proficiency = [90, 80, 85, 75]

plt.figure(figsize=(6,4))
bars = plt.bar(skills, proficiency, color=['#3776AB', '#4479A1', '#FF6F00', '#11557C'])

# Label each bar with its percentage value
for bar, perc in zip(bars, proficiency):
    plt.text(bar.get_x() + bar.get_width() / 2, bar.get_height() + 1, f'{perc}%', ha='center', fontsize=10)

plt.ylim(0, 100)
plt.title('My Skill Proficiency')
plt.xlabel('Skills')
plt.ylabel('Proficiency (%)')
plt.tight_layout()
plt.savefig('skill_chart.png')
