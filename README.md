# Project-self-understanding-and-render-3-description-tables
# DEMO REVIEW
![image](https://github.com/user-attachments/assets/44c5dcec-7810-4a98-9263-cd111b02aaeb)
![image](https://github.com/user-attachments/assets/c1c21236-ab98-4ec8-88d6-38180577a67d)
![image](https://github.com/user-attachments/assets/df6a334d-2e8e-4030-8a1c-756b9dd2487b)
![image](https://github.com/user-attachments/assets/2a8e8e0b-5405-4811-aed8-4a0a25131edb)
![image](https://github.com/user-attachments/assets/320dac78-f698-4207-8560-98ba546beb9d)
![image](https://github.com/user-attachments/assets/0c0d9e86-ffee-45a5-94e9-b294d52542c0)
![image](https://github.com/user-attachments/assets/3fabf08d-a434-4b7d-94be-24706efa7d88)
![image](https://github.com/user-attachments/assets/e34c17da-24b0-4771-a33a-da37cb79bed1)
![image](https://github.com/user-attachments/assets/a57b7278-3942-41ac-92d4-e15c36a00426)
![image](https://github.com/user-attachments/assets/1913dab1-1c78-4481-b03b-24776bbbdf13)
![image](https://github.com/user-attachments/assets/80d4af84-1d6c-485c-a869-aad444eae920)

# 🎯 Personal Insight & Development Tool 📊

This Python-based command-line application is a comprehensive tool for personal self-assessment. It guides users through a series of questions across various personal dimensions, stores their responses, analyzes the data, and generates insightful visualizations. The primary goal is to help individuals gain a deeper understanding of their core values, dominant intelligences, motivations, personal goals, and self-awareness levels.

The tool is designed to display questions and chart labels in Vietnamese.

## ✨ Features

*   **Comprehensive Questionnaire:** 📝 Over 50 questions covering:
    *   Core Values (e.g., Honesty, Fairness, Personal Growth)
    *   Dominant Intelligences (based on Howard Gardner's theory: Linguistic, Logical-Mathematical, Musical, Spatial, Bodily-Kinesthetic, Interpersonal, Intrapersonal, Naturalistic)
    *   Learning & Action Motivations (e.g., Challenge-driven, Goal-oriented, Intrinsic/Extrinsic)
    *   Personal Goals (e.g., Short-term, Long-term, SMART goals)
    *   Self-Awareness Levels (e.g., Strengths, Weaknesses, Emotional Triggers)
*   **Likert Scale Responses:** Users respond on a 1-5 scale (Strongly Disagree to Strongly Agree).
*   **Data Persistence:** 💾 Assessment results are saved as timestamped JSON files for each user.
*   **Result Analysis:** 🔍
    *   Calculates average scores for each specific question type and broader category.
    *   Identifies potential strengths and areas for improvement based on scores.
    *   Provides a simple comparative analysis (e.g., Dominant Intelligences vs. Motivation).
*   **Data Visualization:** 📈
    *   **Radar Chart:** For an overview of scores across main assessment categories.
    *   **Bar Chart:** For detailed comparison of scores within a specific category (e.g., types of intelligences).
    *   **Pie Chart:** To show the proportion of scores within a category (e.g., distribution of core values).
*   **Report Generation:** 📄 Saves generated charts as PNG files. (Future extension could be PDF/HTML reports).
*   **User-Friendly CLI:** 💻 Interactive command-line interface for easy navigation.

## 🛠️ Tech Stack & Requirements

*   **Python 3.x**
*   **Libraries:**
    *   `pandas`: For data manipulation and analysis.
    *   `matplotlib`: For generating charts.
    *   `numpy`: For numerical operations, often a dependency for pandas/matplotlib.
*   **Font:** Arial (or another Vietnamese-supporting font like Tahoma, Times New Roman) must be available on your system for Matplotlib to correctly display Vietnamese characters in charts. If you encounter issues with Vietnamese text in charts, ensure the specified font in the script (`plt.rcParams['font.family'] = 'Arial'`) is installed and accessible.

## ⚙️ Installation

1.  **Clone the repository (or download the script):**
    ```bash
    # If it's a Git repository
    git clone <repository_url>
    cd <repository_directory>
    ```
    If you just have the script, save it as `personal_assessment_tool.py` (or any `.py` name you prefer).

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    # On Windows
    .\venv\Scripts\activate
    # On macOS/Linux
    source venv/bin/activate
    ```

3.  **Install required libraries:**
    ```bash
    pip install pandas matplotlib numpy
    ```

4.  **Font Check:**
    Ensure you have a font like 'Arial' installed that supports Vietnamese characters for the charts.

## ▶️ Usage

1.  **Run the script from your terminal:**
    ```bash
    python personal_assessment_tool.py
    ```
    (Replace `personal_assessment_tool.py` with the actual name of your Python file.)

2.  **Main Menu:**
    You will be presented with the main menu:
    ```
    --- HỆ THỐNG TỰ ĐÁNH GIÁ CÁ NHÂN ---
    1. Thực hiện bài đánh giá mới (Take a new assessment)
    2. Phân tích kết quả đã lưu (Analyze saved results)
    3. Thoát (Exit)
    Nhập lựa chọn của bạn (1-3):
    ```

3.  **Option 1: Take a new assessment**
    *   You'll be prompted to enter your name (e.g., `NguyenVanA`). This name is used for saving the results file.
    *   Answer each question by typing a number from 1 (Hoàn toàn không đồng ý / Rất kém - Strongly Disagree / Very Poor) to 5 (Hoàn toàn đồng ý / Rất tốt - Strongly Agree / Very Good).
    *   After completing all questions, your results will be:
        *   Saved to a JSON file in the `ket_qua_danh_gia/` directory (e.g., `NguyenVanA_20231027_103045.json`).
        *   Analyzed and printed to the console.
        *   Visualized, and charts will be saved as PNG files in the `bieu_do_danh_gia/` directory.

4.  **Option 2: Analyze saved results**
    *   A list of previously saved JSON assessment files from the `ket_qua_danh_gia/` directory will be displayed.
    *   Enter the number corresponding to the file you wish to analyze.
    *   The selected results will be loaded, analyzed, and visualizations will be generated and saved (similar to completing a new assessment).

5.  **Option 3: Exit**
    *   Closes the application.

## 📁 Output Files

*   **Assessment Data:** Saved in `./ket_qua_danh_gia/` directory as `<UserName>_<Timestamp>.json`.
*   **Charts:** Saved in `./bieu_do_danh_gia/` directory as PNG files (e.g., `radar_<UserName>_<Timestamp>.png`, `bar_<Category>_<UserName>_<Timestamp>.png`).

## 🧑‍💻 Author

*   **Tran The Hao**
*   University of Transport Ho Chi Minh City (UTH)

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
