# Ex.No.6 AI-Assisted Programming and Debugging

# Date: 26.11.2026
# Register no : 212224040274

# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

## AI TOOLS REQUIRED

1. ChatGPT
2. Google Gemini
3. Python IDE / VS Code
4. Online Python, C and Java compilers

## EXPLANATION

AI-assisted programming uses Artificial Intelligence tools to generate, analyse, debug and optimize computer programs. In this experiment, different AI tools are used as programming assistants to develop a crop disease classification application.

The experiment involves generating code in Python, C and Java, identifying programming errors, improving code efficiency, explaining time and space complexity, generating unit test cases and comparing AI-generated code with manually written code.

## SELECTED APPLICATION

**Project Title: AI-Based Crop Disease Detection System**

**Problem Statement:**

Farmers face difficulties identifying crop diseases manually. An automated system is required to classify plant leaves as healthy or diseased based on image information and provide suitable preventive recommendations.

For this experiment, a simplified disease classification program is developed using sample leaf features. It is a demonstration of classification logic, not an actual image-based disease detection model.

## 1. PERSONA PATTERN PROMPT

**Prompt:**

Act as an experienced software programmer and AI engineer. Develop a simple crop disease classification application using Python, C and Java. The application should accept leaf symptoms such as yellow spots, brown spots and healthy appearance and classify the leaf as healthy or diseased. Generate clean, understandable and error-free code with suitable comments.

## 2. PYTHON CODE GENERATION

**Prompt given to ChatGPT:**

Write a Python program to classify crop leaves based on their symptoms. If the leaf has yellow spots or brown spots, classify it as diseased; otherwise, classify it as healthy. Include user input and output.

**AI-Generated Python Code:**

```python
def detect_disease(symptom):
    if symptom.lower() in ["yellow spots", "brown spots"]:
        return "Diseased Leaf"
    else:
        return "Healthy Leaf"

symptom = input("Enter leaf symptom: ")

result = detect_disease(symptom)

print("Crop Condition:", result)
```

**Sample Output:**

```text
Enter leaf symptom: yellow spots
Crop Condition: Diseased Leaf
```

## 3. C CODE GENERATION

**Prompt given to Google Gemini:**

Generate a C program to identify whether a crop leaf is healthy or diseased based on the symptom entered by the user. Use conditional statements and string comparison.

**AI-Generated C Code:**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char symptom[50];

    printf("Enter leaf symptom: ");
    scanf("%49s", symptom);

    if (strcmp(symptom, "yellow") == 0 ||
        strcmp(symptom, "brown") == 0) {
        printf("Crop Condition: Diseased Leaf\n");
    }
    else {
        printf("Crop Condition: Healthy Leaf\n");
    }

    return 0;
}
```

**Sample Output:**

```text
Enter leaf symptom: yellow
Crop Condition: Diseased Leaf
```

## 4. JAVA CODE GENERATION

**Prompt given to ChatGPT:**

Write a Java program to classify a crop leaf based on its symptoms. Accept user input and use if-else conditions to identify whether the leaf is healthy or diseased.

**AI-Generated Java Code:**

```java
import java.util.Scanner;

public class CropDisease {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        System.out.print("Enter leaf symptom: ");
        String symptom = sc.nextLine().toLowerCase();

        if (symptom.equals("yellow spots") ||
            symptom.equals("brown spots")) {
            System.out.println("Crop Condition: Diseased Leaf");
        }
        else {
            System.out.println("Crop Condition: Healthy Leaf");
        }

        sc.close();
    }
}
```

**Sample Output:**

```text
Enter leaf symptom: brown spots
Crop Condition: Diseased Leaf
```

## 5. BUG IDENTIFICATION AND DEBUGGING

The generated programs were analysed to identify possible errors.

| Bug Identified | Description | Solution |
|---|---|---|
| Case sensitivity | Uppercase and lowercase inputs may produce different results | Convert input to lowercase |
| Incorrect input handling | C program initially accepts only one word | Use `fgets()` for complete input |
| Invalid symptoms | Unknown symptoms may be classified as healthy | Add an invalid-input condition |
| String comparison | C requires `strcmp()` for string comparison | Use `strcmp()` instead of `==` |
| Input validation | Empty input may produce incorrect classification | Check whether input is empty |

## 6. OPTIMIZED PYTHON CODE

The original Python code can be improved by adding input validation and support for multiple symptoms.

```python
def detect_disease(symptom):

    symptom = symptom.lower().strip()

    if not symptom:
        return "Invalid Input"

    diseased = ["yellow spots", "brown spots"]

    if symptom in diseased:
        return "Diseased Leaf"

    elif symptom == "healthy":
        return "Healthy Leaf"

    else:
        return "Unknown Symptom"

symptom = input("Enter leaf symptom: ")

print("Crop Condition:", detect_disease(symptom))
```

**Sample Output:**

```text
Enter leaf symptom: Yellow Spots
Crop Condition: Diseased Leaf
```

## 7. TIME AND SPACE COMPLEXITY ANALYSIS

| Operation | Time Complexity | Space Complexity |
|---|---|---|
| Input reading | O(n) | O(n) |
| String comparison | O(n) | O(1) additional |
| Disease classification | O(1) for fixed-size symptom list | O(1) |
| Overall classification | O(n) | O(n) including input storage |

Here, n represents the length of the input symptom. The number of disease categories is considered fixed.

## 8. UNIT TEST CASE GENERATION

The following test cases are used to verify the Python program.

| Test Case | Input | Expected Output |
|---|---|---|
| 1 | yellow spots | Diseased Leaf |
| 2 | brown spots | Diseased Leaf |
| 3 | healthy | Healthy Leaf |
| 4 | Yellow Spots | Diseased Leaf |
| 5 | unknown | Unknown Symptom |
| 6 | Empty input | Invalid Input |

## 9. COMPARISON OF MULTIPLE AI TOOLS

| Evaluation Criteria | ChatGPT | Google Gemini |
|---|---|---|
| Code generation | Generates structured code | Generates structured code |
| Explanation | Provides detailed explanations | Provides detailed explanations |
| Debugging | Identifies syntax and logical errors | Suggests debugging improvements |
| Optimization | Suggests code improvements | Suggests alternative implementations |
| Unit testing | Generates test cases | Generates test cases |

## 10. MANUAL CODING VS AI-ASSISTED CODING

| Criteria | Manual Coding | AI-Assisted Coding |
|---|---|---|
| Code generation | Written manually | Generated using AI prompts |
| Development time | Generally takes more time | Can reduce development time |
| Debugging | Programmer identifies errors | AI suggests possible corrections |
| Code optimization | Requires programming knowledge | AI suggests improvements |
| Unit testing | Written manually | AI can generate test cases |
| Learning | Improves independent coding skills | Helps understand coding concepts |
| Accuracy | Depends on programmer | Requires verification by programmer |

## 11. CODE QUALITY ANALYSIS

The generated Python, C and Java programs were analysed based on readability, correctness, efficiency and maintainability.

- **Readability:** AI-generated programs contain simple syntax and meaningful variable names.
- **Correctness:** The programs perform the required symptom-based classification for the specified inputs.
- **Efficiency:** The classification process uses simple conditional statements and has low computational overhead.
- **Maintainability:** Functions and comments make the programs easier to understand and modify.
- **Reliability:** Input validation and unit testing help identify possible errors.

AI-generated code must always be reviewed and tested before practical implementation.

## CONCLUSION

AI-assisted programming improves the software development process by reducing repetitive coding work and helping programmers identify errors and optimize programs. Comparing ChatGPT and Google Gemini demonstrated that multiple AI tools can provide different coding approaches and debugging suggestions.

The experiment also showed that AI-generated code requires manual verification and testing to ensure correctness and reliability. Thus, AI tools act as effective programming assistants while the programmer remains responsible for validating the final solution.

# Result: The corresponding Prompt is executed successfully.
