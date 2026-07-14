# Walkthrough Video Script (2-Minute Screen Run)

**Title**: Josh Talks AI - Human Evaluation for Text-to-Image Indian Clothing Models  
**Duration**: 2 Minutes (120 Seconds)  
**Speaker Tone**: Professional, energetic, product-focused  

---

### Segment 1: Problem Statement & Context (0:00 - 0:20)
*   **Visual**: Screen starts on the Cover and TOC page of `index.html` (the A4 Research Report). Cursor highlights the title.
*   **Audio (Narration)**:
    > "Hello, my name is Anjali Garg. In this video, I will present my project on human evaluation benchmarks for text-to-image AI models generating Indian ethnic clothing. 
    >
    > Traditional automated metrics like FID are insufficient because they fail to capture critical cultural nuances, such as correct drape styles, intricate fabric textures, and jewelry placement. This evaluation bridges that gap through structured human feedback."

---

### Segment 2: Evaluation Design & Models (0:20 - 0:35)
*   **Visual**: Scroll to page 8 ("Models Evaluated") and page 9 ("Prompt Design") in the PDF report, pointing out the side-by-side prompt benchmarks.
*   **Audio (Narration)**:
    > "To benchmark performance, we evaluated three models: GPT Image 1, Gemini 2.5 Flash, and Gemini 2.5 Flash Preview. 
    >
    > We generated clothing images across three distinct prompts specifying detailed Indian outfits—such as a mustard yellow kurti with white embroidery and a pink silk anarkali. Every model was tested under identical prompts to guarantee absolute fairness."

---

### Segment 3: Human Evaluation Process (0:35 - 0:55)
*   **Visual**: Switch tab to the live web application (`evaluation.html`). Show the participant details entry form, and then fill in a demo evaluation rating stars on a prompt (showing side-by-side Model A, B, and C).
*   **Audio (Narration)**:
    > "Here is our live evaluation portal. Evaluators enter their demographics—such as age and familiarity with ethnic wear—before scoring images.
    >
    > To prevent cognitive bias, the interface dynamically shuffles the placement of model outputs, labeling them anonymized as Model A, B, and C. Evaluators grade each output out of 5 stars across five key dimensions, including cultural accuracy and fabric detail."

---

### Segment 4: Admin Analytics Dashboard (0:55 - 1:15)
*   **Visual**: Click on the 'Admin Dashboard' view in the portal. Hover over the real-time sync count, and point to the Chart.js visual breakdowns (Model Scores bar chart, Demographic pie charts).
*   **Audio (Narration)**:
    > "Upon submitting ratings, data syncs instantly with Google Firestore. In the Admin Dashboard, we see live statistical aggregations. 
    >
    > Using Chart.js, we display real-time performance breakdowns, participant cultural familiarity, and age distribution. Admins can also run data diagnostics, reload seed data, or export results directly to a CSV file."

---

### Segment 5: Results & Insights (1:15 - 1:35)
*   **Visual**: Switch back to `index.html` page 13 ("Results & Insights"). Highlight the table showing the score comparison and winner medals.
*   **Audio (Narration)**:
    > "Based on our 12-participant evaluation dataset, GPT Image 1 was the overall winning model with an average score of 4.8 out of 5, leading in prompt adherence and e-commerce layout readiness. 
    >
    > Gemini 2.5 Flash Preview scored 4.5, outperforming others in realism and natural fabric folds. Gemini 2.5 Flash was the fastest but was critiqued for simplified patterns."

---

### Segment 6: Key Reflections & Closing (1:35 - 2:00)
*   **Visual**: Scroll to page 16 ("Reflection"). Point out the cards summarizing personal learnings and the value of localized datasets for Indian AI labs.
*   **Audio (Narration)**:
    > "This project demonstrates that high-realism does not guarantee cultural accuracy. AI labs building foundational models for India must establish localized benchmarks rather than relying on generic Western sets. 
    >
    > In the future, I plan to scale this workflow by introducing randomized blind testing panels and automated visual pre-screening using Vision-Language Models. Thank you for watching!"
