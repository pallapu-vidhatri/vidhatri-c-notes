<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>C Lang - C Programming Notes by Pallapu Vidhatri</title>
<style>
  /* Reset & base */
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'Segoe UI', Tahoma, sans-serif;
    background: #f9f9f7;
    color: #333;
    line-height: 1.6;
  }
  a { color: #2a7ae2; text-decoration: none; }
  a:hover { text-decoration: underline; }

  /* Header */
  header {
    background: #e3e6e1;
    padding: 1.2rem 2rem;
    text-align: center;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  }
  header h1 { color: #2a7ae2; margin-bottom: 0.2rem; }
  header p { color: #555; font-style: italic; }

  /* Layout */
  main { display: flex; min-height: 90vh; }
  nav {
    width: 250px;
    background: #f0f1ec;
    border-right: 1px solid #ccc;
    padding: 1rem;
    overflow-y: auto;
    position: sticky; top: 0; height: 90vh;
  }
  nav h2 { font-size: 1.2rem; margin-bottom: 1rem; color: #2a7ae2; }
  nav ul { list-style: none; }
  nav li { margin-bottom: 0.6rem; }
  nav a { font-weight: 600; font-size: 0.95rem; }
  nav a.active { color: #1a4db7; font-weight: 700; }

  section.content {
    flex: 1;
    padding: 2rem 3rem;
    background: #fff;
    margin: 1rem;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.05), inset 0 0 10px #f0f1ec;
  }

  /* Page style */
  .page {
    background: #fffef8;
    border: 1px solid #ddd;
    padding: 1.6rem 2rem;
    border-radius: 6px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    max-width: 900px;
    margin: 0 auto 2rem auto;
    transition: transform 0.6s ease;
  }

  /* Headings */
  h2 { color: #2a7ae2; border-bottom: 2px solid #2a7ae2; padding-bottom: 0.3rem; margin: 1.5rem 0 1rem; }
  h3 { color: #1a4db7; margin-top: 1.2rem; }

  /* Code blocks */
  pre, code {
    background: #f4f4f4;
    border-radius: 4px;
    font-family: 'Courier New', monospace;
    font-size: 0.9rem;
  }
  pre { padding: 1rem; overflow-x: auto; margin: 1rem 0; }
  .keyword { color: #d73a49; font-weight: bold; }
  .datatype { color: #005cc5; font-weight: bold; }
  .comment { color: #6a737d; font-style: italic; }
  .string { color: #032f62; }

  /* Tables */
  table { border-collapse: collapse; width: 100%; margin: 1rem 0 2rem; }
  th, td { border: 1px solid #ccc; padding: 0.5rem 0.8rem; }
  th { background: #e3e6e1; }

  /* Flowchart */
  .flowchart-symbols { display: flex; flex-wrap: wrap; gap: 1.5rem; margin: 1rem 0 2rem; }
  .symbol { flex: 1 1 120px; text-align: center; }
  .symbol svg { width: 80px; height: 60px; margin-bottom: 0.3rem; }

  /* Quotes */
  blockquote {
    font-style: italic;
    border-left: 4px solid #2a7ae2;
    margin: 1.5rem 0;
    padding-left: 1rem;
    background: #f0f1ec;
    border-radius: 4px;
  }

  /* Footer */
  footer {
    background: #e3e6e1;
    padding: 1rem 2rem;
    text-align: right;
    font-size: 0.9rem;
    color: #555;
    font-style: italic;
  }

  /* Responsive */
  @media (max-width: 900px) {
    main { flex-direction: column; }
    nav { width: 100%; height: auto; border-bottom: 1px solid #ccc; }
    section.content { margin: 1rem; padding: 1.2rem; }
  }
</style>
</head>
<body>

<header>
  <h1>C Lang</h1>
  <p>C Programming Language Notes by Pallapu Vidhatri</p>
</header>

<main>
  <nav>
    <h2>Contents</h2>
    <ul id="toc">
      <li><a href="#intro-c">Introduction</a></li>
      <li><a href="#block-diagram">Block Diagram</a></li>
      <li><a href="#io-components">I/O Components</a></li>
      <li><a href="#c-applications">Applications</a></li>
      <li><a href="#flowchart-c">Flowchart Example</a></li>
      <li><a href="#flowchart-symbols">Flowchart Symbols</a></li>
      <li><a href="#algorithm">Algorithm</a></li>
      <li><a href="#pseudocode">Pseudocode</a></li>
      <li><a href="#keywords-identifiers">Keywords & Identifiers</a></li>
      <li><a href="#constants-literals">Constants & Literals</a></li>
      <li><a href="#data-types">Data Types</a></li>
      <li><a href="#type-conversion">Type Conversion & ASCII</a></li>
      <li><a href="#operators">Operators</a></li>
      <li><a href="#input-output">Input/Output</a></li>
      <li><a href="#conditional-statements">Conditionals</a></li>
      <li><a href="#loops">Loops</a></li>
      <li><a href="#strings-functions">Strings & Functions</a></li>
      <li><a href="#arrays-pointers-structures">Arrays, Pointers & Structures</a></li>
    </ul>
  </nav>

  <section class="content">

    <!-- Intro -->
    <article id="intro-c" class="page">
      <h2>Introduction to C Language</h2>
      <p>C is a powerful general-purpose programming language developed by Dennis Ritchie in 1972...</p>
      <blockquote>“C is the mother of all programming languages.” – Dennis Ritchie</blockquote>
      <ul>
        <li>Procedural programming language</li>
        <li>Low-level access to memory</li>
        <li>Portable and efficient</li>
        <li>Supports structured programming</li>
      </ul>
    </article>

    <!-- Block Diagram -->
    <article id="block-diagram" class="page">
      <h2>Block Diagram of Computer and CPU</h2>
      <p>A computer consists of input devices, output devices, memory, CPU, and storage...</p>
      <img src="https://i.imgur.com/6Xq6XqG.png" style="max-width:100%;border:1px solid #ccc;border-radius:6px;">
    </article>

    <!-- Input/Output Components -->
    <article id="io-components" class="page">
      <h2>Input and Output Components</h2>
      <p><strong>Input:</strong> keyboard, mouse, scanner<br><strong>Output:</strong> monitor, printer, speakers</p>
    </article>

    <!-- Applications -->
    <article id="c-applications" class="page">
      <h2>Applications of C</h2>
      <ul><li>Operating Systems</li><li>Embedded Systems</li><li>Compilers</li><li>Databases</li></ul>
    </article>

    <!-- Example flowchart -->
    <article id="flowchart-c" class="page">
      <h2>C Program Flowchart Example</h2>
      <pre><code>
#include &lt;stdio.h&gt;
int main() {
  int a, b, sum;
  scanf("%d%d", &a, &b);
  sum = a + b;
  printf("Sum = %d", sum);
  return 0;
}
      </code></pre>
      <img src="https://i.imgur.com/7Q6XqGZ.png" style="max-width:100%;border:1px solid #ccc;border-radius:6px;">
    </article>

    <!-- Flowchart Symbols -->
    <article id="flowchart-symbols" class="page">
      <h2>Flowchart Symbols</h2>
      <div class="flowchart-symbols">
        <div class="symbol"><svg><rect width="80" height="40" x="10" y="10" fill="#2a7ae2" stroke="#1a4db7"/></svg><p><b>Process</b></p></div>
        <div class="symbol"><svg><polygon points="50,10 90,30 50,50 10,30" fill="#2a7ae2" stroke="#1a4db7"/></svg><p><b>Decision</b></p></div>
      </div>
    </article>

    <!-- Algorithm -->
    <article id="algorithm" class="page">
      <h2>Algorithm</h2>
      <ol><li>Start</li><li>Read A,B</li><li>SUM=A+B</li><li>Print SUM</li><li>End</li></ol>
    </article>

    <!-- Pseudocode -->
    <article id="pseudocode" class="page">
      <h2>Pseudocode</h2>
      <pre><code>
START
  INPUT A
  INPUT B
  SUM = A + B
  OUTPUT SUM
END
      </code></pre>
    </article>

    <!-- Keywords -->
    <article id="keywords-identifiers" class="page">
      <h2>Keywords and Identifiers</h2>
      <pre><code>
int age;
float salary;
char name[20];
      </code></pre>
    </article>

    <!-- Constants -->
    <article id="constants-literals" class="page">
      <h2>Constants and Literals</h2>
      <pre><code>
const int max = 100;
const float pi = 3.14;
const char grade = 'A';
      </code></pre>
    </article>

    <!-- Data Types -->
    <article id="data-types" class="page">
      <h2>Data Types</h2>
      <table>
        <tr><th>Type</th><th>Example</th></tr>
        <tr><td>int</td><td>42</td></tr>
        <tr><td>float</td><td>3.14</td></tr>
        <tr><td>char</td><td>'A'</td></tr>
      </table>
    </article>

    <!-- Type Conversion -->
    <article id="type-conversion" class="page">
      <h2>Type Conversion & ASCII</h2>
      <pre><code>
char c = 'A';
printf("%d", c); // prints 65
      </code></pre>
    </article>

    <!-- Operators -->
    <article id="operators" class="page">
      <h2>Operators</h2>
      <ul><li>Arithmetic: +, -, *, /, %</li><li>Relational: &lt;, &gt;, ==</li><li>Logical: &&, ||, !</li></ul>
    </article>

    <!-- Input/Output -->
    <article id="input-output" class="page">
      <h2>Input & Output</h2>
      <pre><code>
scanf("%d", &num);
printf("Value=%d", num);
      </code></pre>
    </article>

    <!-- Conditionals -->
    <article id="conditional-statements" class="page">
      <h2>Conditional Statements</h2>
      <pre><code>
if (a > b) printf("A larger");
else printf("B larger");
      </code></pre>
    </article>

    <!-- Loops -->
    <article id="loops" class="page">
      <h2>Loop Statements</h2>
      <pre><code>
for (int i=0; i&lt;5; i++) {
  printf("%d ", i);
}
      </code></pre>
    </article>

    <!-- Strings & Functions -->
    <article id="strings-functions" class="page">
      <h2>Strings & Functions</h2>
      <pre><code>
void greet() { printf("Hello!"); }
int main(){ greet(); return 0; }
      </code></pre>
    </article>

    <!-- Arrays, Pointers, Structures -->
    <article id="arrays-pointers-structures" class="page">
      <h2>Arrays, Pointers & Structures</h2>
      <pre><code>
int arr[3] = {1,2,3};
int *p = arr;
struct Student { char name[20]; int age; };
      </code></pre>
    </article>

  </section>
</main>

<footer>
  &copy; 2025 Pallapu Vidhatri | C Programming Notes
</footer>

<script>
  // Highlight active section in sidebar
  const sections = document.querySelectorAll("article");
  const navLinks = document.querySelectorAll("nav a");

  window.addEventListener("scroll", () => {
    let current = "";
    sections.forEach(sec => {
      const top = sec.offsetTop - 120;
      if (pageYOffset >= top) current = sec.getAttribute("id");
    });
    navLinks.forEach(a => {
      a.classList.remove("active");
      if (a.getAttribute("href").includes(current)) a.classList.add("active");
    });
  });
</script>

</body>
</html>
