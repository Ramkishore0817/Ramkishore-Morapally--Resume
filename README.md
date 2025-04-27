# Ramkishore Morapally--Resume
%%%%
% MTecknology's Resume
%%%%
% Author: Michael Lustfield
% License: CC-BY-4
% - https://creativecommons.org/licenses/by/4.0/legalcode.txt
%%%%

\documentclass[letterpaper,10pt]{article}
%%%%%%%%%%%%%%%%%%%%%%%
%% BEGIN_FILE: mteck.sty
%% NOTE: Everything between here and END_FILE can
%% be relocated to "mteck.sty" and then included with:
%\usepackage{mteck}

% Dependencies
% NOTE: Some packages (lastpage, hyperref) require second build!
\usepackage[empty]{fullpage}
\usepackage{titlesec}
\usepackage{enumitem}
\usepackage[hidelinks]{hyperref}
\usepackage{fancyhdr}
\usepackage{fontawesome5}
\usepackage{multicol}
\usepackage{bookmark}
\usepackage{lastpage}

% Sans-Serif
%\usepackage[sfdefault]{FiraSans}
%\usepackage[sfdefault]{roboto}
%\usepackage[sfdefault]{noto-sans}
%\usepackage[default]{sourcesanspro}

% Serif
\usepackage{CormorantGaramond}
\usepackage{charter}

% Colors
% Use with \color{Name}
% Can wrap entire heading with {\color{accent} [...] }
\usepackage{xcolor}
\definecolor{accentTitle}{HTML}{0e6e55}
\definecolor{accentText}{HTML}{0e6e55}
\definecolor{accentLine}{HTML}{a16f0b}

% Misc. Options
\pagestyle{fancy}
\fancyhf{}
\fancyfoot{}
\renewcommand{\headrulewidth}{0pt}
\renewcommand{\footrulewidth}{0pt}
\urlstyle{same}

% Adjust Margins
\addtolength{\oddsidemargin}{-0.7in}
\addtolength{\evensidemargin}{-0.5in}
\addtolength{\textwidth}{1.19in}
\addtolength{\topmargin}{-0.7in}
\addtolength{\textheight}{1.4in}

\setlength{\multicolsep}{-3.0pt}
\setlength{\columnsep}{-1pt}
\setlength{\tabcolsep}{0pt}
\setlength{\footskip}{3.7pt}
\raggedbottom
\raggedright

% ATS Readability
\input{glyphtounicode}
\pdfgentounicode=1

%-----------------%
% Custom Commands %
%-----------------%

% Centered title along with subtitle between HR
% Usage: \documentTitle{Name}{Details}
\newcommand{\documentTitle}[2]{
  \begin{center}
    {\Huge\color{accentTitle} #1}
    \vspace{10pt}
    {\color{accentLine} \hrule}
    \vspace{2pt}
    %{\footnotesize\color{accentTitle} #2}
    \footnotesize{#2}
    \vspace{2pt}
    {\color{accentLine} \hrule}
  \end{center}
}

% Create a footer with correct padding
% Usage: \documentFooter{\thepage of X}
\newcommand{\documentFooter}[1]{
  \setlength{\footskip}{10.25pt}
  \fancyfoot[C]{\footnotesize #1}
}

% Simple wrapper to set up page numbering
% Usage: \numberedPages
% WARNING: Must run pdflatex twice!
\newcommand{\numberedPages}{
  \documentFooter{\thepage/\pageref{LastPage}}
}

% Section heading with horizontal rule
% Usage: \section{Title}
\titleformat{\section}{
  \vspace{-5pt}
  \color{accentText}
  \raggedright\large\bfseries
}{}{0em}{}[\color{accentLine}\titlerule]

% Section heading with separator and content on same line
% Usage: \tinysection{Title}
\newcommand{\tinysection}[1]{
  \phantomsection
  \addcontentsline{toc}{section}{#1}
  {\large{\bfseries\color{accentText}#1} {\color{accentLine} |}}
}

% Indented line with arguments left/right aligned in document
% Usage: \heading{Left}{Right}
\newcommand{\heading}[2]{
  \hspace{10pt}#1\hfill#2\\
}

% Adds \textbf to \heading
\newcommand{\headingBf}[2]{
  \heading{\textbf{#1}}{\textbf{#2}}
}

% Adds \textit to \heading
\newcommand{\headingIt}[2]{
  \heading{\textit{#1}}{\textit{#2}}
}

% Template for itemized lists
% Usage: \begin{resume_list} [items] \end{resume_list}
\newenvironment{resume_list}{
  \vspace{-7pt}
  \begin{itemize}[itemsep=-2px, parsep=1pt, leftmargin=30pt]
}{
  \end{itemize}
  %\vspace{-2pt}
}

% Formats an item to use as an itemized title
% Usage: \itemTitle{Title}
\newcommand{\itemTitle}[1]{
  \item[] \underline{#1}\vspace{4pt}
}

% Bullets used in itemized lists
\renewcommand\labelitemi{--}

%% END_FILE: mteck.sty
%%%%%%%%%%%%%%%%%%%%%%


%===================%
% John Doe's Resume %
%===================%

%\numberedPages % NOTE: lastpage requires a second build
%\documentFooter{\thepage of 2} % Does similar without using lastpage
\begin{document}

  %---------%
  % Heading %
  %---------%

  \documentTitle{Ram Kishore Morapally}{
    % Web Version
    %\raisebox{-0.05\height} \faPhone\ [redacted - web copy] ~
    %\raisebox{-0.15\height} \faEnvelope\ [redacted - web copy] ~
    %%
    \href{tel:9110723746}{
      \raisebox{-0.05\height} \faPhone\ 9110723746} ~ | ~
    \href{mailto:ramkishorereddy13218@gmaiI.com}{
      \raisebox{-0.15\height} \faEnvelope\ ramkishorereddy13218@gmaiI.com } ~ | ~
    \href{https://www.linkedin.com/in/morapally-ramkishore-reddy-556552170/}{
      \raisebox{-0.15\height} \faLinkedin\ linkedin.com/in/ram-kishore/} ~ | ~
    \href{https://github.com/Ramkishore0817}{
      \raisebox{-0.05\height} \faGithub\ github.com/ram-kishore}\\
      \raisebox{-0.15\height} \faHome\ Warangal-bhupalpalle, Hyderabad, Telangana, 506168
  }

  %---------%
  % Summary %
  %---------%

\section{Summary}
Experienced Automation Engineer with over 3.5 years of expertise in building and implementing robust automation frameworks using Python. I have hands-on experience across the complete Software Testing Life Cycle (STLC), including requirement analysis, test planning, test case development, environment setup, test execution, and defect management. I am skilled in analyzing business needs, creating functional specifications, and developing comprehensive test strategies. I have maintained and configured automated test scripts and environments, executed and debugged test cases, and effectively managed defect workflows. I work well with clients, providing timely updates, troubleshooting issues, and delivering accurate solutions.

  %--------%
  % Skills %
  %--------%

\section{Skills}

\textbf{Technical Skills}\\
\begin{itemize}
    \item \textbf{Programming \& Scripting:} Python, Object-Oriented Programming (OOP), CAPL scripting, Shell scripting
    \item \textbf{Testing Frameworks \& Methodologies:} Pytest, unittest, Functional Testing, Black Box Testing, Agile/Scrum, STLC
    \item \textbf{Tools \& Environments:} Git,
    Jira,Polarion,Linux, PyCharm, Visual Studio, AutomationDesk,
    ControlDesk, Vector CANalyzer
    \item \textbf{Protocols \& Interfaces:} CAN Protocol, ADB (Android Debug Bridge),J1939,LIN,UDS.
    \item \textbf{Data \& Web Processing:} Pandas, NumPy, BeautifulSoup, Requests
    \item \textbf{Computer Vision \& Image Processing:} OpenCV, Tesseract, Image Preprocessing,Openpyxl
    \item \textbf{Domain-Specific Tools:} Dspace Tools, Panel Designing, Embedded System Testing
\end{itemize}

\textbf{Soft Skills}\\
Problem-solving, Team Collaboration, Adaptability, Analytical Thinking, Attention to Detail, Communication





  %------------%
  % Experience %
  %------------%

 \section{Experience}

\headingBf{L\&T Technology Services}{Aug 2021 -- Present}
\headingIt{Engineer | Embedded and Automation Testing}{}  
\begin{resume_list}
\item Developed and maintained automation test scripts using \textbf{Python} in \textbf{PyCharm} for embedded systems and \textbf{HIL} setups using \textbf{dSPACE AutomationDesk} and \textbf{ControlDesk}.
\item Built Python-based automation frameworks to support functional and regression testing, ensuring faster validation of embedded software releases.
\item Performed \textbf{Black Box} and \textbf{Functional Testing} for embedded systems and Android-based displays for agricultural machinery like tractors and sprayers.
\item Automated test workflows integrating Python scripts with \textbf{AutomationDesk}, reducing manual testing efforts by 40\%.
\item Created and executed test cases for \textbf{CAN} and \textbf{J1939} protocol communication scenarios using \textbf{CAPL scripting} and \textbf{Vector CANalyzer}.
\item Diagnosed and resolved CAN communication issues by analyzing logs using custom Python tools and \textbf{CANalyzer} traces.
\item Developed OpenCV-based Python tools for display validation and graphical interface testing on Android systems.
\item Integrated \textbf{Tesseract OCR} with automation scripts to validate text rendering in display testing.
\item Wrote custom Python scripts to automate validation of system logs, ensuring compliance with technical specifications and project standards.
\item Designed and validated system panels for \textbf{HIL} setups, ensuring efficient sensor-actuator simulation and system interaction.
\item Utilized \textbf{pytest} and \textbf{unittest} frameworks to create scalable and reusable automated test cases.
\item Conducted performance and stress testing on embedded controllers under various simulated environmental conditions.
\item Built automation utilities for real-time monitoring and reporting of system performance during testing phases.
\item Collaborated with development teams to design \textbf{MATLAB simulation models} for testing automotive control logic.
\item Participated actively in Agile/Scrum practices, including sprint planning, daily stand-ups, and retrospectives.
\item Documented detailed test strategies, automation scripts, defect analysis reports, and CAN configuration files.
\item Recognized with "\textbf{Star of the Month}" award for outstanding contributions to automation initiatives and project deliveries.
\item Provided mentoring and technical support to junior engineers on Python scripting, automation frameworks, and CAN testing methodologies.


\end{resume_list}





  %-----------%
  % Education %
  %-----------%

\section{Education}

\headingBf{Bachelor of Technology, Computer Science and Engineering}{2017--2021}
\headingIt{Lovely Professional University, Phagwara, Punjab }{}
\vspace{4pt}

\headingBf{Pre-University Course (MPC)}{2015--2017}
\headingIt{SR Junior College, Warangal, Telangana }{}
\vspace{4pt}

\headingBf{Secondary School Certificate (SSC)}{2015}
\headingIt{St. Mathews High School, Karimnagar, Telangana }{}




  %----------------------------%
  % Extracurricular Activities %
  %----------------------------%

  \section{Projects}

\headingBf{Hospital Management System Website}{Feb 2018}
\begin{resume_list}
\item Designed and developed a basic Hospital Management website for storing and retrieving hospital, staff, and patient records.
\item Utilized HTML, CSS, and JavaScript to build a responsive and accessible frontend, allowing users to access key hospital information and contact details with ease.
\end{resume_list}

\headingBf{Mini ATM Machine Simulation}{Dec 2017}
\begin{resume_list}
\item Created a simple ATM simulation program using C language to calculate and track user transactions including credit, debit, and balance inquiry operations.
\item Implemented core logic for managing multiple accounts, providing a foundational understanding of transactional systems in banking.
\end{resume_list}


   \section{Certifications and Achievements}
\vspace{4pt}
\begin{resume_list}


\item Honored with the "\textbf{Star of the Month}" award for achieving key \textbf{automation testing milestones} and driving \textbf{process improvements}.
\item Certified in \textbf{Robotic Process Automation (RPA)} using \textbf{Automation Anywhere} (2018–2019), with hands-on experience in \textbf{automation workflow design}.
\item Successfully completed an \textbf{R Programming} course on \textbf{Coursera} (2020), focusing on \textbf{statistical computing} and \textbf{data analysis}.
\item Completed a \textbf{Digital Marketing} course on \textbf{Coursera} (2021), enhancing understanding of \textbf{automation in digital tools and processes}.

\end{resume_list}


\end{document}
