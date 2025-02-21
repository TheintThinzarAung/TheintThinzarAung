# generate_chart.py
import matplotlib.pyplot as plt

# Example skill names and proficiency percentages
skills = ['Python', 'SQL', 'Machine Learning', 'Data Visualization']
proficiency = [90, 80, 85, 75]

plt.figure(figsize=(8, 5))
bars = plt.bar(skills, proficiency, color=['#3776AB', '#4479A1', '#FF6F00', '#11557C'])

# Add percentage labels above each bar
for bar, perc in zip(bars, proficiency):
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width() / 2, yval + 1, f'{perc}%', ha='center', va='bottom', fontsize=10)

plt.ylim(0, 100)
plt.title('My Skill Proficiency')
plt.xlabel('Skills')
plt.ylabel('Proficiency (%)')
plt.tight_layout()
plt.savefig('skill_chart.png')  # Save as PNG
