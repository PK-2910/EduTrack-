# feedback_entry.py

def collect_feedback():
    feedback_data = []
    while True:
        name = input("Enter student name (or 'done' to finish): ")
        if name.lower() == 'done':
            break
        try:
            score = float(input(f"Enter score for {name} (0-100): "))
        except ValueError:
            print("Invalid score. Try again.")
            continue
        feedback_data.append({'name': name, 'score': score})
    return feedback_data

if __name__ == "__main__":
    feedback = collect_feedback()
    print("Collected Feedback:", feedback)
