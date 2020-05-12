%-------------------------------------
% LaTeX Resume for Software Engineers
% Author : Leslie Cheng
% License : MIT
%-------------------------------------

\documentclass[a4paper,12pt]{article}[leftmargin=*]
\usepackage[empty]{fullpage}
\usepackage{enumitem}
\usepackage{ifxetex}
\ifxetex
  \usepackage{fontspec}
  \usepackage[xetex]{hyperref}
\else
  \usepackage[utf8]{inputenc}
  \usepackage[T1]{fontenc}
  \usepackage[pdftex]{hyperref}
\fi
\usepackage{fontawesome}
\usepackage[sfdefault,light]{FiraSans}
\usepackage{anyfontsize}
\usepackage{xcolor}
\usepackage{tabularx}

%-------------------------- SETTINGS HERE --------------------------
% Header settings
\def \fullname {Saeed Vayghani}
\def \subtitle {Senior Software Engineer}

\def \linkedinicon {\faLinkedin}
\def \linkedinlink {https://www.linkedin.com/in/saeed-vayghani-b2866939/}
\def \linkedintext {/saeed-vayghani}

\def \phoneicon {\faPhone}
\def \phonetext {(Iran) +xx-xxxxxxx}

\def \skypeicon {\faSkype}
\def \skypetext {live:xxxxx}

\def \emailicon {\faEnvelope}
\def \emaillink {mailto:xxxx@gmail.com}
\def \emailtext {xxxx@gmail.com}

\def \githubicon {\faGithub}
\def \githublink {https://github.com/saeed-vayghan}
\def \githubtext {Github}

\def \websiteicon {\faStackOverflow}
\def \websitelink {https://stackoverflow.com/users/11074334/saeed}
\def \websitetext {Stackoverflow}

\def \headertype {\doublecol} % \singlecol or \doublecol

% Misc settings
\def \entryspacing {-0pt}

\def \bulletstyle {\faAngleRight}

% Define colours
\definecolor{primary}{HTML}{000000}
\definecolor{secondary}{HTML}{0D47A1}
\definecolor{accent}{HTML}{263238}
\definecolor{links}{HTML}{1565C0}

%------------------------------------------------------------

% Defines to make listing easier
\def \linkedin {\linkedinicon \hspace{3pt}\href{\linkedinlink}{\linkedintext}}
\def \phone {\phoneicon \hspace{3pt}{ \phonetext}}
\def \skype {\skypeicon \hspace{3pt}{\skypetext}}
\def \email {\emailicon \hspace{3pt}\href{\emaillink}{\emailtext}}
\def \github {\githubicon \hspace{3pt}\href{\githublink}{\githubtext}}
\def \website {\websiteicon \hspace{3pt}\href{\websitelink}{\websitetext}}

% Adjust margins
\addtolength{\oddsidemargin}{-0.55in}
\addtolength{\evensidemargin}{-0.55in}
\addtolength{\textwidth}{1.1in}
\addtolength{\topmargin}{-0.7in}
\addtolength{\textheight}{1.1in}

% Define the link colours
\hypersetup{
    colorlinks=true,
    urlcolor=links,
}

% Set the margin alignment 
\raggedbottom
\raggedright
\setlength{\tabcolsep}{0in}

%-------------------------
% Custom commands

% Sections
\renewcommand{\section}[2]{\vspace{5pt}
  \colorbox{secondary}{\color{white}\raggedbottom\normalsize\textbf{{#1}{\hspace{7pt}#2}}}
}

% Entry start and end, for spacing
\newcommand{\resumeEntryStart}{\begin{itemize}[leftmargin=2.5mm]}
\newcommand{\resumeEntryEnd}{\end{itemize}\vspace{\entryspacing}}

% Itemized list for the bullet points under an entry, if necessary
\newcommand{\resumeItemListStart}{\begin{itemize}[leftmargin=4.5mm]}
\newcommand{\resumeItemListEnd}{\end{itemize}}

% Resume item
\renewcommand{\labelitemii}{\bulletstyle}
\newcommand{\resumeItem}[1]{
  \item\small{
    {#1 \vspace{-2pt}}
  }
}

% Entry with title, subheading, date(s), and location
\newcommand{\resumeEntryTSDL}[4]{
  \vspace{-1pt}\item[]
    \begin{tabularx}{0.99\textwidth}{X@{\hspace{60pt}}r}
      \textbf{\color{primary}#1} & {\firabook\color{accent}\small#2} \\
      \textit{\color{accent}\small#3} & \textit{\color{accent}\small#4} \\
    \end{tabularx}\vspace{-7pt}
}

% Entry with title and date(s)
\newcommand{\resumeEntryTD}[2]{
  \vspace{-1pt}\item[]
    \begin{tabularx}{0.97\textwidth}{X@{\hspace{60pt}}r}
      \textbf{\color{primary}#1} & {\firabook\color{accent}\small#2} \\
    \end{tabularx}\vspace{-6pt}
}

% Entry for special (skills)
\newcommand{\resumeEntryS}[2]{
  \item[]\small{
    \textbf{\color{primary}#1 }{ #2 \vspace{-6pt}}
  }
}

% Double column header
\newcommand{\doublecol}[6]{
  \begin{tabularx}{\textwidth}{Xr}
    {
      \begin{tabular}[c]{l}
        \fontsize{35}{45}\selectfont{\color{primary}{{\textbf{\fullname}}}} \\
        {\textit{\subtitle}} % You could add a subtitle here
      \end{tabular}
    } & {
      \begin{tabular}[c]{l@{\hspace{1.5em}}l}
        {\small#4} & {\small#1} \\
        {\small#5} & {\small#2} \\
        {\small#6} & {\small#3}
      \end{tabular}
    }
  \end{tabularx}
}

% Single column header
\newcommand{\singlecol}[6]{
  \begin{tabularx}{\textwidth}{Xr}
    {
      \begin{tabular}[b]{l}
        \fontsize{35}{45}\selectfont{\color{primary}{{\textbf{\fullname}}}} \\
        {\textit{\subtitle}} % You could add a subtitle here
      \end{tabular}
    } & {
      \begin{tabular}[c]{l}
        {\small#1} \\
        {\small#2} \\
        {\small#3} \\
        {\small#4} \\
        {\small#5} \\
        {\small#6}
      \end{tabular}
    }
  \end{tabularx}
}

\begin{document}
%-------------------------- BEGIN HERE --------------------------

%-------------------------- HEADER ------------------------------

\headertype{\linkedin}{\github}{\website}{\phone}{\skype}{\email}{} % Set the order of items here
\vspace{-5pt} % Set a negative value to push the body up, and the opposite

%-------------------------- EXPERIENCE --------------------------
\vspace{5pt}
\section{\faPieChart}{Experience}
  \resumeEntryStart
    \vspace{-7pt}
    \resumeEntryTSDL
      {\href{https://rechat.com/}{Rechat Inc} - Senior Backend Engineer}{2019 -- Present}
      {Rechat is an intuitive CRM and marketing platform for real estate professionals.}
      {Austin, US (Remotely)}
    \resumeItemListStart
      \resumeItem {Having a significant \textbf{positive impact} on  \textbf{customers experience} by implementing Google and Microsoft two-way sync services}
      \resumeItem {Working on a high quality product in an \textbf{international team} with smart people from different countries}
      \resumeItem {Implement a Node.js crawler to login, search, and retrieve reports in behalf of users}
      \resumeItem {Implement a pure JS Throttler and Debouncer to optimize webhooks processing and decrease the DB-IO}
      \resumeItem {Participate in a team to build processes to get the security license powered by BishopFox}
    \resumeItemListEnd
  \resumeEntryEnd
  
  \vspace{-15pt}
  \resumeEntryStart
    \resumeEntryTSDL
      {\href{https://www.linkedin.com/company/navaak/about/}{Navaak Inc} - Co Founder and Backend Engineer}{2013 -- 2019}
      {Navaak is a music streaming service like Spotify. Navaak became one of the winners in IBridge 2015 and now is the market leader in Iran’s music streaming industry.}{Tehran, Iran}
    \resumeItemListStart
      \resumeItem {Hire, coach and manage a team of software developers}
      \resumeItem {Develop company's  \textbf{culture} on top of respect and transparency to deliver a world class platform}
      \resumeItem {Reduce the infrastructure cost \textbf{up to 40 percent} by implementing a Redis \textbf{caching} layer}
      \resumeItem {Lead a team to design and launch a Linux based \textbf{Infrastructure architecture} (multi-datacenter)}
      \resumeItem {Implement a \textbf{multi-layer logging} and backup services to address potential outages}
      \resumeItem {Develop Node.js \textbf{REST-Full} API servers influenced by \textbf{Micro-Services}}
      \resumeItem {Develop a \textbf{messaging system} on top of RabbitMQ in order to have a \textbf{persistent} backbone}
      \resumeItem {Develop several \textbf{rate limiters} to decrease the cost of third-party services}
      \resumeItem {Develop an \textbf{Analytics} system on top of ELK which helps to increase users session time \textbf{up to 20 percent}}
      \resumeItem {\textbf{Document} the system knowledge base (references available upon request)}
    \resumeItemListEnd
  \resumeEntryEnd

  \vspace{-15pt}
  \resumeEntryStart
    \resumeEntryTSDL
      {\href{https://www.lognumber.com}{Lognumber} - Full Stack Developer}{2013 -- 2019}
      {It is an educational game for kids to learn logical thinking of numbers. It was \textbf{my first international project} and let me learn how to communicate with remote manager.}{Tehran, Iran}
    \resumeItemListStart
        \resumeItem {HTML/CSS/Js, PHP/MYSQL}
    \resumeItemListEnd
  \resumeEntryEnd
  
  \vspace{-14pt}
  \resumeEntryStart
    \resumeEntryTSDL
      {University of Tabriz - Full Stack Developer}{2012 -- 2013}
      {Design and implement a web-based course registration systems, It helped the faculty to have a \textbf{better understanding} of students needs to provide them with \textbf{proper timetable}.}{Tehran, Iran}
    \resumeItemListStart
        \resumeItem {PHP/MYSQL}
    \resumeItemListEnd
  \resumeEntryEnd

  \vspace{-14pt}
  \resumeEntryStart
    \resumeEntryTSDL
      {Armaghan Rahe Talaie - Full Stack Developer}{2011 -- 2012}
      {I managed to \textbf{decrease the cost} of controlling the users ACLs by Developing a panel}{Tehran, Iran}
    \resumeItemListStart
      \resumeItem {PHP Slim framework, MySQL}
    \resumeItemListEnd
  \resumeEntryEnd


%-------------------------- PROGRAMMING SKILLS --------------------------
\section{\faGears} {Software Skills}
 \resumeEntryStart
  \resumeEntryS
    {Understanding of:}
    {Concurrency, Functional Programing, OOP, SOLID, 12 Factors, Unit and Functional Testing, Debugging, Teamwork, Problem solving}
  
  \resumeEntryS
    {Experience with:}
    {\color{black} JavaScript, Node.js (Express.js), PHP, SQL, PostgreSQL, MongoDB, Elasticsearch, Redis, RabbitMQ, SOAP, REST, GraphQL, Git, Docker, Google-APIs, Microsoft-Graph-APIs, Scrum, Kanban}
 \resumeEntryEnd


%-------------------------- Open Source --------------------------
\vspace{2pt}
\section{\faGears} {Open Source Projects}
 \resumeEntryStart
  \resumeEntryS
    {}
    {
        {\href{https://github.com/saeed-vayghan/Data-Structure}{Collection of pure JS data-structure}} -
        {\href{https://github.com/saeed-vayghan/google-microsoft-two-way-sync}{An open implementation of Google and Microsoft two-way sync}}
    }
 \resumeEntryEnd
 

%-------------------------- EDUCATION --------------------------
\vspace{2pt}
\section{\faGraduationCap}{Education}
  \resumeEntryStart
    \vspace{-10pt}
    \resumeEntryTSDL
      {University of Tabriz}{2007 -- 2011}
      {Bachelor Degree in Computer/Software Engineering}
      {Tabriz, Iran}
  \resumeEntryEnd

\end{document}
