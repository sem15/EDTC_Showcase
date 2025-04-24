<template>
    <div id="showcase-app">
      <header class="app-header">
        <div class="header-content">
          <h1>Authoring Systems for Instructional Product Development</h1>
          <nav class="main-nav">
            <ul>
              <li :class="{ active: currentPage === 'home' }">
                <button @click="currentPage = 'home'">Home</button>
              </li>
              <li :class="{ active: currentPage === 'evaluations' }">
                <button @click="currentPage = 'evaluations'">Software Evaluations</button>
              </li>
              <li :class="{ active: currentPage === 'nearpod' }">
                <button @click="currentPage = 'nearpod'">Nearpod Tutorial</button>
              </li>
              <li :class="{ active: currentPage === 'ai-literacy' }">
                <button @click="currentPage = 'ai-literacy'">AI Literacy</button>
              </li>
              <li :class="{ active: currentPage === 'mini-project' }">
                <button @click="currentPage = 'mini-project'">Mini Project</button>
              </li>
            </ul>
          </nav>
        </div>
      </header>

      <main class="app-main">
        <transition name="fade" mode="out-in">
          <div v-if="currentPage === 'home'" key="home" class="page-content home-page">
            <h2>Welcome!</h2>
            <p>This website showcases the work I completed during this section of {{ courseTitle }}.</p>
            <figure class="home-image-container">
              <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=MnwzNjUyOXwwfDF8c2VhcmNofDN8fGNvZGluZ3xlbnwwfHx8fDE2ODAxNjQyOTU&ixlib=rb-4.0.3&q=80&w=1080" alt="Laptop with code on screen" />
              <figcaption>
                Image by <a href="https://unsplash.com/@flouffy?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText" target="_blank" rel="noopener noreferrer">Fotis Fotopoulos</a> on <a href="https://unsplash.com/s/photos/coding?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText" target="_blank" rel="noopener noreferrer">Unsplash</a>
              </figcaption>
            </figure>
             <p>Navigate through the sections using the menu above to explore each assignment I completed.</p>
          </div>

          <div v-else-if="currentPage === 'evaluations'" key="evaluations" class="page-content">
            <h2>Software Evaluations</h2>
            <p>Here are evaluations of two instructional programs based on the criteria provided in the course:</p>

            <div class="evaluation-section">
              <h3>Evaluation: Egg Drop Interactive</h3>
              <p><strong>URL:</strong> <a href="https://www.physicsclassroom.com/Physics-Interactives/Momentum-and-Collisions/Egg-Drop/Egg-Drop-Interactive" target="_blank" rel="noopener noreferrer">https://www.physicsclassroom.com/Physics-Interactives/Momentum-and-Collisions/Egg-Drop/Egg-Drop-Interactive</a></p>
              <div class="table-container">
                <table>
                  <thead>
                    <tr>
                      <th>Criterion</th>
                      <th>Rating</th>
                      <th>Comments</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>Instructional Effectiveness</td>
                      <td>Satisfactory</td>
                      <td>The simulation provides all relevant information about the physics behind the action, but that’s about all it does. It doesn’t really guide the user at all, but rather simulates an experiment. I would potentially offer some guidance after a simulation has been run to possibly push the learner closer to the solution without giving too much away.</td>
                    </tr>
                    <tr>
                      <td>Instructional Efficiency</td>
                      <td>Very Good</td>
                      <td>The instruction was very easy to use. The simulation has a graphical display that helps immerse the student in the exercise. After the action concludes and the egg lands, the math and status of the egg is displayed, providing a nice summary of the experiment. The design of the GUI is very intuitive and I had no difficulty navigating any part of the courseware.</td>
                    </tr>
                    <tr>
                      <td>Inspiration</td>
                      <td>Very Good</td>
                      <td>The design of this insertional content did keep me engaged. Since I felt like I had full control, I was interested enough to view all possibly outcomes. The graphical display of the experiment changed slightly with each set of conditions which kept me entertained while I was interacting with it. As someone who learns by experimenting and viewing, this courseware appealed to me.</td>
                    </tr>
                    <tr>
                      <td>Reflections</td>
                      <td>Good</td>
                      <td>I felt totally in control of the learning experience, but in a sense I felt like that may have detracted from the learning aspect slightly. I sort of ignored the math and drew my own conclusions based on the outcome of the egg. Overall, I would recommend this to others as it was interesting and well designed over all. If I had to advise change, I would maybe add some kind of dialogue over all that guided the learner between different attempts. This dialogue could also highlight aspects of the math portion that have changed between attempts. What learner engagement feature might you incorporate into instruction that you design and develop for EDTC 6030?</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>

            <div class="evaluation-section">
              <h3>Evaluation: World Continents</h3>
              <p><strong>URL:</strong> <a href="https://world-geography-games.com/en/world_continents.html" target="_blank" rel="noopener noreferrer">https://world-geography-games.com/en/world_continents.html</a></p>
              <div class="table-container">
                <table>
                  <thead>
                    <tr>
                      <th>Criterion</th>
                      <th>Rating</th>
                      <th>Comments</th>
                    </tr>
                  </thead>
                  <tbody>
                     <tr>
                      <td>Instructional Effectiveness</td>
                      <td>Good</td>
                      <td>Overall, the software doesn’t really assist the user. The user gets unlimited attempts and their only feedback is a wrong sound or a right sound upon clicking a continent. The user can just view the solution at any time.</td>
                    </tr>
                    <tr>
                      <td>Instructional Efficiency</td>
                      <td>Very Good</td>
                      <td>The instruction was extremely basic and easy to use. The design was very easy to understand and I have trouble imagining that anyone would have difficulty using the courseware. The sound design consisted of two different sounds, which I guess is pretty efficient, but leads to a very basic experience.</td>
                    </tr>
                    <tr>
                      <td>Inspiration</td>
                      <td>Satisfactory</td>
                      <td>I didn’t really feel engaged at all while using this courseware. Some people may feel a very slight satisfaction at coloring in the world by answering questions, but it feels pretty weak to me. (I have to admit that my view is a little biased since I am already very familiar with the course content. This might work a little better with someone learning this for the first time. I updated my score from weak to Satisfactory.)</td>
                    </tr>
                    <tr>
                      <td>Reflections</td>
                      <td>Satisfactory</td>
                      <td>I felt like I was in complete control of the learning experience, but to the point where I could just view the answers immediately without having to try at all. I think if I was struggling to get the answers correct, after a certain point I could get hints perhaps, but just showing the answers immediately seems a bit too easy for a course that has barely any substance to begin with. I might recommend the course to be used at like a first grade level perhaps, but even then I think a better product could be designed. A possible feature I would add could be a hint system of some kind to keep the learner engaged. I certainly wouldn’t just have a “Solution” button available from the beginning. What learner engagement feature might you incorporate into instruction that you design and develop for EDTC 6030?</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>

          <div v-else-if="currentPage === 'nearpod'" key="nearpod" class="page-content nearpod-page revised-nearpod">
            <h2>Nearpod Tutorial</h2>
            <p>
              In Nearpod, I created a lesson for the following instructional context, which identifies the target learners and specifies the instructional objectives. In addition, a description of the instructional method appears below.
            </p>

            <div class="context-section">
              <h3>Target Learners</h3>
              <p>Senior Citizens and those new to using technology.</p>
            </div>

            <div class="context-section">
              <h3>Instructional Objectives</h3>
              <p>After the instruction, the learners will be able to demonstrate the following capabilities:</p>
              <ul>
                <li>Compress a file on Windows.</li>
                <li>Extract a file on Windows.</li>
                <li>Describe the effects of basic file compression.</li>
              </ul>
            </div>

            <div class="context-section">
               <h3>Instructional Method</h3>
               <p>Each learner will view a video, an image, and an audio clip supported by a narrative, then they will test their knowledge briefly via a check on learning question.</p>
            </div>

            <a href="https://np1.nearpod.com/sharePresentation.php?code=0adfe01f7e4384c47394a59a0a106505-1&oc=user-created&utm_source=link"
               target="_blank"
               rel="noopener noreferrer"
               class="nearpod-image-wrapper-link"
               title="Link to Nearpod Tutorial">
              <img :src="fileCompressionImg"
                   alt="Illustration of file compression"
                   class="nearpod-direct-image" />
            </a>
            <p class="nearpod-click-instruction">
                (Click the image above to view the lesson)
            </p>

            <div class="nearpod-join-code-section">
              <p>
                <strong>Nearpod Join Code:</strong> <strong class="join-code">V9RYD</strong>
              </p>
            </div>
            </div>
          <div v-else-if="currentPage === 'ai-literacy'" key="ai-literacy" class="page-content">
            <h2>AI Literacy</h2>

            <section>
              <h3>Conception of AI Literacy</h3>
              <p>
                Based on the AI Literacy Framework paper and personal reflection, an AI literate person should primarily know and apply ethical standards when using AI, recognizing its potential for misuse. It's important to understand what not to do before engaging deeply with AI. Furthermore, an AI literate individual should be able to conceptually separate the AI from a human, understanding its limitations to avoid pitfalls like hallucinations. This involves recognizing that framing the AI's 'identity' or role within a prompt is a vital skill for effective general-purpose use.
              </p>
            </section>

            <section>
              <h3>Lessons Learned from Instructional Development Prompts</h3>
              <p>
                Using AI chatbots (like Google Gemini and ChatGPT) to generate instructional content provided several insights into effective prompting and AI capabilities:
              </p>
              <ul>
                <li>**Initial Output Quality:** AI can produce impressively detailed and comprehensive lesson plans even from general prompts, often including relevant components like learning objectives and exercises. For simpler topics like file compression, the initial output can be quite satisfactory and usable.</li>
                <li>**Need for Specificity and Refinement:** While initial outputs can be strong outlines, they often require follow-up prompts to tailor the content to specific needs, such as adjusting the learning level or focus (e.g., historical vs. mathematical aspects). AI might provide guidance on creating exercises rather than the exercise itself, requiring further prompting.</li>
                <li>**AI Limitations and "Corner Cutting":** For more complex or nuanced tasks, like creating interactive web-based lessons (HTML/CSS/JS) for figurative language, the AI might generate valid basic code but create simplistic or less effective learning content, potentially "cutting corners" by relying on basic checks rather than deeper interaction.</li>
                <li>**Iterative Process:** Generating truly effective instructional content often requires reviewing the AI's output and using iterative prompting to refine and improve the lesson, saving time on the initial drafting but still requiring human oversight and adjustment.</li>
                 <li>**Helpful Explanations:** AI can effectively explain concepts at a beginner level and include practical tips relevant to the instruction.</li>
              </ul>
            </section>
          </div>

          <div v-else-if="currentPage === 'mini-project'" key="mini-project" class="page-content">
            <h2>Mini Project: AI-Assisted Web App Development</h2>
            <p>
              For the mini-project, I chose to create a web application primarily because I enjoy the process and wanted to test the capabilities of the updated Google Gemini 2.5 model in developing a VueJS app, specifically one involving Google Firebase integration. My goal was to explore how effectively a functional and relatively complex application could be developed almost entirely through AI prompting, using an iterative, feature-by-feature approach rather than large, single prompts. This was relevant to my professional interest in AI's potential to assist with programming tasks.
            </p>
            <p>
              The process involved extensive prompting (estimated 50-75 prompts) to generate code for features, handle styling, and implement Firebase functionality. While the AI wasn't perfect, it proved capable of producing functional code, especially impressing with the Firebase integration. Key learnings involved the effectiveness of detailed, specific prompts ("acting like a tyrant") to guide the AI and limit errors, while still allowing some creative latitude for aspects like layout and color palettes, followed by iterative refinement.
            </p>
            <div class="project-link-container">
              <p>You can view the resulting web application here:</p>
              <a href="https://sem15.github.io/EDTC_MiniProject/" target="_blank" rel="noopener noreferrer" class="project-link-button">Capitals Mini Project</a>
            </div>
          </div>

        </transition>
      </main>

      <footer class="app-footer">
        <p>&copy; {{ new Date().getFullYear() }} [Steven Maxwell] - {{ courseTitle }}</p>
      </footer>
    </div>
  </template>

  <script>
  // Import the local image
  import fileCompressionImg from '@/assets/filecompression.png'; // Assumes '@' alias points to 'src'

  export default {
    name: 'App',
    data() {
      return {
        courseTitle: 'EDTC 6030',
        currentPage: 'home', // Initial page to display
        // Make the imported image available in the template
        fileCompressionImg: fileCompressionImg
      };
    },

  };
  </script>

  <style>
  /* --- Global Styles & Color Palette --- */
  :root {
    /* Cool Palette Example (Adjust as desired) */
    --bg-primary: #f4f7f6; /* Very light grey-blue */
    --bg-secondary: #ffffff; /* White */
    --bg-header: #34495e; /* Wet Asphalt - Complements the active blue */
    --text-primary: #333333; /* Dark Grey */
    --text-secondary: #555555; /* Medium Grey */
    --text-header: #ecf0f1; /* Light Grey/Almost White */
    --accent-primary: #3498db; /* Bright Blue */
    --accent-primary-darker: #2980b9; /* Darker Blue for hover */
    --border-color: #e0e0e0; /* Light Grey Border */
    --shadow-color: rgba(0, 0, 0, 0.1);
    --table-header-bg: #e9ecef; /* Light grey for table header */
    --link-color: var(--accent-primary);
    --link-hover-color: var(--accent-primary-darker);
    --button-bg: var(--accent-primary);
    --button-text: #ffffff; /* Ensure button text is white */
    --button-hover-bg: var(--accent-primary-darker);

    /* Font */
    --font-sans: 'Poppins', 'Helvetica Neue', Arial, sans-serif;
  }

  /* Import Google Font */
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap');


  /* Basic Reset */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  html {
    font-size: 16px; /* Base font size */
  }

  body {
    font-family: var(--font-sans);
    line-height: 1.6;
    color: var(--text-primary);
    background-color: var(--bg-primary);
    margin: 0;
  }

  #showcase-app {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  /* --- Header --- */
  .app-header {
    background-color: var(--bg-header);
    color: var(--text-header);
    padding: 1rem 0;
    box-shadow: 0 2px 4px var(--shadow-color);
    position: sticky;
    top: 0;
    z-index: 1000;
    width: 100%;
  }

  .header-content {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .app-header h1 {
    font-size: 1.8rem;
    font-weight: 600;
    margin-bottom: 0.75rem;
    text-align: center;
  }

  /* --- Navigation --- */
  .main-nav ul {
    list-style: none;
    display: flex;
    flex-wrap: wrap; /* Allow wrapping on smaller screens */
    justify-content: center;
    gap: 0.5rem; /* Spacing between items */
  }

  .main-nav li button {
    font-family: inherit;
    background: none;
    border: none;
    color: var(--text-header);
    padding: 0.6rem 1rem;
    cursor: pointer;
    font-size: 1rem;
    font-weight: 500;
    border-radius: 4px;
    transition: background-color 0.2s ease, color 0.2s ease;
    text-align: center;
  }

  .main-nav li button:hover {
    background-color: rgba(255, 255, 255, 0.1);
    color: #ffffff;
  }

  .main-nav li.active button {
    background-color: var(--accent-primary);
    color: #ffffff;
    font-weight: 600;
  }

  /* --- Main Content Area --- */
  .app-main {
    flex-grow: 1;
    width: 100%;
    max-width: 1100px;
    margin: 2rem auto; /* Top/bottom margin, auto left/right */
    padding: 0 1.5rem;
  }

  .page-content {
    background-color: var(--bg-secondary);
    padding: 2rem 2.5rem;
    border-radius: 8px;
    box-shadow: 0 3px 10px var(--shadow-color);
    border: 1px solid var(--border-color);
  }

  .page-content h2 {
    font-size: 1.75rem;
    color: var(--bg-header); /* Use header color for headings */
    margin-bottom: 1.5rem;
    font-weight: 600;
    border-bottom: 2px solid var(--accent-primary);
    padding-bottom: 0.5rem;
    display: inline-block; /* Make border only as wide as text */
  }

  .page-content h3 {
      font-size: 1.4rem;
      color: var(--text-primary);
      margin-top: 1.5rem;
      margin-bottom: 0.75rem;
      font-weight: 600;
  }

  /* Style added for spacing between evaluation sections */
  .evaluation-section {
      margin-bottom: 2.5rem; /* Add space below each evaluation table section */
  }
  .evaluation-section:last-child {
      margin-bottom: 0; /* Remove margin from the last section */
  }

  .evaluation-section p {
      margin-bottom: 0.5rem; /* Reduce margin below the URL paragraph */
  }


  .page-content p,
  .page-content li {
    margin-bottom: 1rem;
    color: var(--text-secondary);
  }

  .page-content ul, .page-content ol {
      padding-left: 2rem; /* Indent lists */
  }

  .page-content ul {
      list-style: disc; /* Ensure bullets are shown for objectives */
  }


  .page-content li {
      margin-bottom: 0.5rem;
  }

  .page-content a {
      color: var(--link-color);
      text-decoration: none;
      transition: color 0.2s ease;
  }

  .page-content a:hover {
      color: var(--link-hover-color);
      /* Default link underline removed from here, handled by button style */
      /* text-decoration: underline; */
  }

  /* Specific Page Styles */
  .home-page {
      text-align: center;
  }

  .home-image-container {
      margin: 2rem auto;
      max-width: 600px;
  }

  .home-image-container img {
      display: block;
      max-width: 100%;
      height: auto;
      border-radius: 6px;
      box-shadow: 0 2px 8px var(--shadow-color);
      margin: 0 auto;
  }

  .home-image-container figcaption {
      font-size: 0.85rem;
      color: var(--text-secondary);
      margin-top: 0.5rem;
      font-style: italic;
      text-align: center;
  }

  /* Nearpod Page Specific Styles */
  .nearpod-page.revised-nearpod {
      text-align: left;
  }

  .nearpod-page .context-section {
      margin-bottom: 1.5rem;
  }

  .nearpod-page .context-section h3 {
      margin-top: 0;
      margin-bottom: 0.5rem;
      font-size: 1.25rem;
      color: var(--bg-header);
  }

  .nearpod-page .context-section p,
  .nearpod-page .context-section ul {
      margin-bottom: 0;
  }
  .nearpod-page .context-section ul {
      padding-left: 2.5rem;
  }

  /* Styling for the directly placed image */
  .nearpod-direct-image {
      display: block;
      max-width: 600px;
      height: auto;
      margin: 2rem auto 0.5rem auto;
      border: 1px solid var(--border-color);
      border-radius: 6px;
      box-shadow: 0 2px 8px var(--shadow-color);
      transition: opacity 0.2s ease; /* Keep transition for hover effect */
  }

  /* Styling for the wrapper link around the image */
  .nearpod-image-wrapper-link {
      display: block; /* Make link block to contain image */
      text-decoration: none;
      margin-bottom: 0; /* Remove space below link */
      text-align: center; /* Center the image within the link block */
  }
  .nearpod-image-wrapper-link:hover .nearpod-direct-image {
      opacity: 0.8; /* Fade image slightly on hover */
  }

  /* Styling for the added click instruction */
  .nearpod-click-instruction {
      text-align: center;
      font-size: 0.9rem;
      font-style: italic;
      color: var(--text-secondary);
      margin-top: 0.75rem; /* Space above instruction */
      margin-bottom: 2rem; /* Space below instruction before join code */
  }

  /* Styling for the join code section */
   .nearpod-join-code-section {
      text-align: center;
      margin-top: 2rem; /* Keep margin from image/caption */
      padding: 1rem;
      background-color: #f8f9fa;
      border: 1px solid var(--border-color);
      border-radius: 6px;
  }
   .nearpod-join-code-section p {
       margin-bottom: 0;
   }

  .join-code {
      font-family: monospace;
      background-color: #e9ecef;
      padding: 0.2em 0.5em;
      border-radius: 4px;
      font-size: 1.2em;
      color: var(--text-primary);
      border: 1px solid #ced4da;
  }

  /* Mini Project Page Specific Styles */
  .project-link-container {
      margin-top: 2rem;
      text-align: center;
  }

  .project-link-container p {
      margin-bottom: 0.75rem;
  }

  .page-content a.project-link-button {
      display: inline-block;
      background-color: var(--button-bg);
      color: var(--button-text);
      padding: 0.8rem 1.8rem;
      border-radius: 25px;
      text-decoration: none;
      border: none;
      cursor: pointer;
      font-weight: 500;
      font-size: 1.1rem;
      box-shadow: 0 2px 5px rgba(0,0,0,0.15);
      transition: transform 0.15s ease;
  }

  .page-content a.project-link-button:hover {
      background-color: var(--button-hover-bg);
      color: var(--button-text);
      text-decoration: none;
      transform: translateY(-2px);
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }
  .page-content a.project-link-button:active {
      transform: translateY(0px);
      box-shadow: 0 2px 5px rgba(0,0,0,0.15);
  }


  /* --- Table Styling --- */
  .table-container {
      overflow-x: auto;
      margin-top: 1rem;
      border: 1px solid var(--border-color);
      border-radius: 6px;
  }

  table {
      width: 100%;
      border-collapse: collapse;
      min-width: 600px;
  }

  th, td {
      padding: 0.9rem 1rem;
      text-align: left;
      border-bottom: 1px solid var(--border-color);
      vertical-align: top;
  }

  td:nth-child(2) {
      font-weight: 500;
      min-width: 100px;
  }


  thead th {
      background-color: var(--table-header-bg);
      font-weight: 600;
      color: var(--text-primary);
      font-size: 0.95rem;
      border-bottom-width: 2px;
  }

  tbody tr:nth-child(even) {
      background-color: #f8f9fa;
  }

  tbody tr:hover {
      background-color: #e9ecef;
  }

  td:first-child, th:first-child {
      font-weight: 500;
  }

  /* --- AI Literacy Section Styling --- */
  .page-content section {
      margin-bottom: 2rem;
  }
  .page-content section ul {
      list-style: disc;
      padding-left: 2.5rem;
  }

  /* --- Footer --- */
  .app-footer {
    background-color: #e9ecef;
    color: var(--text-secondary);
    text-align: center;
    padding: 1rem;
    margin-top: 2rem;
    font-size: 0.9rem;
    border-top: 1px solid var(--border-color);
  }

  /* --- Transitions --- */
  .fade-enter-active, .fade-leave-active {
    transition: opacity 0.3s ease;
  }
  .fade-enter-from, .fade-leave-to {
    opacity: 0;
  }

  /* --- Responsive Adjustments --- */
  @media (max-width: 768px) {
    .app-header h1 {
      font-size: 1.5rem;
    }

    .main-nav li button {
        font-size: 0.9rem;
        padding: 0.5rem 0.8rem;
    }

    .app-main {
      margin: 1.5rem auto;
      padding: 0 1rem;
    }

    .page-content {
      padding: 1.5rem;
    }

    .page-content h2 {
      font-size: 1.5rem;
    }
     .page-content h3 {
      font-size: 1.25rem;
    }

    th, td {
        padding: 0.7rem 0.8rem;
    }
  }

  @media (max-width: 480px) {
    html {
        font-size: 15px;
    }

    .app-header h1 {
      font-size: 1.3rem;
    }

    .main-nav ul {
        gap: 0.2rem;
    }
    .main-nav li button {
        font-size: 0.85rem;
        padding: 0.4rem 0.6rem;
    }

    .app-main {
      margin: 1rem auto;
      padding: 0 0.5rem;
    }

     .page-content {
      padding: 1rem;
    }

    .page-content h2 {
      font-size: 1.3rem;
    }
     .page-content h3 {
      font-size: 1.15rem;
    }

    th, td {
        padding: 0.6rem 0.5rem;
    }

     .project-link-button {
          font-size: 1rem;
          padding: 0.7rem 1.5rem;
      }
      /* Adjust direct image size */
      .nearpod-direct-image {
          max-width: 90%;
      }
      .join-code {
          font-size: 1.1em;
      }
  }

  </style>