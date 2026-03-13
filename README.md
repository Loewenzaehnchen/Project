# :world_map: Ecotourism Travel Recommendation System

A GUI-based travel recommendation system that suggests a Central American country based on a user's ecological interests and activities.
The program collects user input (age, interests, preferred activities), calculates a score, recommends a destination, and displays activity suggestions along with visual graphs.

---
## :grey_question: How It Works
1. User enters age
2. User selects two main interests
3. User chooses activities related to those interests
4. System calculates a total score based on a predetermined dictionary
5. Score chooses a Central American country
6. Recommended activities are displayed
7. Visual graphs show score breakdowns

---

## *Classes*

### :one: TravelerInput

- Handles the user's input and creates a score for them

**Main attributes:**

- `age` — user's age
- `interests` — selected interest categories
- `selected_activities` — chosen activities
- `total_score` — calculated score

**Main methods:**

- `collect_age()` — screen where user inputs age
- `collect_interests()` — interest selection
- `collect_activities()` — activity selection
- `submit_selection()` — score calculation
- `get_country()` — determines recommended country

---

### :two: TravellerOutput

- This class displays the final recommendation

**Main attributes:**

- `result_window` — Tkinter window showing results
- `country` — recommended destination country
- Access to traveler data:
  - `total_score`
  - `selected_activities`
  - `Countries_dictionary`

**Main methods:**

- `display_result(traveler)`
  - Creates the result window
  - Displays recommended country
  - Shows total score
  - Embeds graphs using Matplotlib
  - Calls `ActivityRecommender` for suggestions
  - Applies background image
---

### :three: ActivityRecommender

- Provides specific suggestions on what to do in the country that the user received

**Main attributes:**

- `activity_database` — dictionary mapping

**Main methods:**

- `recommend(traveler, result_window)`
  - Retrieves the recommended country
  - Looks up activities in the database
  - Filters suggestions based on user's selected activities
  - Displays recommendations in the result window
  - Formats suggestions in a readable list

---

## :computer: Outputs

<!-- OUTPUT PICTURE HERE -->

![First page](images/output.png)
![Second page](images/output.png)
![Third page](images/output.png)
![Final page](images/output.png)

---

## :paperclip: Requirements

In order to run the code you will need to install matplotlib in Windows Powershell

```bash
pip install matplotlib
