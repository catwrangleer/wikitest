:root {
    --bg-color: #0d1117;
    --card-bg: #161b22;
    --text-main: #c9d1d9;
    --text-muted: #8b949e;
    --accent: #58a6ff;
    --accent-strong: #79c0ff;
    --border-color: #30363d;
    --highlight: #f7d774;
    --success: #7ee787;
}

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    background-color: var(--bg-color);
    color: var(--text-main);
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    line-height: 1.6;
    padding: 2rem 0;
}

img {
    max-width: 100%;
    display: block;
}

button {
    font: inherit;
}

.container {
    max-width: 960px;
    margin: 0 auto;
    padding: 0 1.5rem;
}

header {
    margin-bottom: 2rem;
    text-align: center;
}

header h1 {
    font-size: 2.5rem;
    color: #ffffff;
    margin-bottom: 0.5rem;
}

header p {
    color: var(--text-muted);
    font-size: 1.2rem;
}

main {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

.card {
    background-color: var(--card-bg);
    border: 1px solid var(--border-color);
    border-radius: 8px;
    padding: 2rem;
}

h2 {
    color: #ffffff;
    margin-bottom: 1rem;
    font-size: 1.5rem;
}

.project-list {
    list-style: none;
    display: grid;
    gap: 0.85rem;
}

.project-list li {
    border-left: 3px solid var(--accent);
    padding-left: 1rem;
}

.page-nav {
    display: flex;
    justify-content: center;
    gap: 0.75rem;
    flex-wrap: wrap;
    margin-top: 1rem;
}

.nav-button,
.link-button,
.project-list a,
.video-link {
    color: var(--accent-strong);
    text-decoration: none;
    transition: opacity 0.2s ease;
}

.nav-button,
.link-button {
    display: inline-block;
    background-color: rgba(88, 166, 255, 0.12);
    border: 1px solid var(--border-color);
    border-radius: 999px;
    padding: 0.65rem 1rem;
    font-weight: 600;
}

.nav-button:hover,
.link-button:hover,
.project-list a:hover,
.video-link:hover {
    opacity: 0.85;
    text-decoration: underline;
}

.gallery-grid,
.video-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1.25rem;
}

.gallery-card,
.video-card {
    background-color: rgba(13, 17, 23, 0.5);
    border: 1px solid var(--border-color);
    border-radius: 8px;
    overflow: hidden;
}

.gallery-card img {
    width: 100%;
    height: 220px;
    object-fit: cover;
}

.gallery-card figcaption,
.video-card .video-meta {
    padding: 0.9rem 1rem;
    color: var(--text-main);
}

.video-card iframe {
    width: 100%;
    min-height: 220px;
    border: 0;
    background: #000;
}

.video-meta p {
    margin-top: 0.35rem;
    color: var(--text-muted);
}

.video-link {
    display: inline-block;
    margin-top: 0.75rem;
    font-weight: 600;
}

.score-text {
    font-size: 1.15rem;
    margin-bottom: 1rem;
}

.game-area {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 1rem;
    margin-bottom: 1rem;
}

.cat-button {
    background: none;
    border: 1px solid var(--border-color);
    border-radius: 12px;
    overflow: hidden;
    cursor: pointer;
    padding: 0;
    transition: transform 0.15s ease, box-shadow 0.15s ease;
}

.cat-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 18px rgba(0,0,0,0.2);
}

.cat-button img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.cat-button:focus-visible {
    outline: 2px solid var(--highlight);
    outline-offset: 2px;
}

.game-actions {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
    align-items: center;
}

.mini-game {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
}

.mini-game-copy,
.quiz-status,
.quiz-question {
    color: var(--text-main);
}

.memory-board {
    display: grid;
    grid-template-columns: repeat(4, minmax(65px, 1fr));
    gap: 0.75rem;
    margin-top: 0.5rem;
}

.memory-card {
    aspect-ratio: 1 / 1;
    border: 1px solid var(--border-color);
    border-radius: 12px;
    background: linear-gradient(135deg, rgba(88, 166, 255, 0.15), rgba(121, 192, 255, 0.05));
    color: #fff;
    font-size: 2rem;
    cursor: pointer;
    transition: transform 0.15s ease, background 0.2s ease;
}

.memory-card:hover {
    transform: translateY(-2px);
}

.memory-card.matched {
    background: rgba(126, 231, 135, 0.2);
    border-color: rgba(126, 231, 135, 0.8);
}

.memory-win {
    grid-column: 1 / -1;
    color: var(--success);
    font-weight: 700;
    margin-top: 0.5rem;
}

.quiz-options {
    display: grid;
    gap: 0.75rem;
}

.quiz-option {
    background: rgba(88, 166, 255, 0.08);
    border: 1px solid var(--border-color);
    border-radius: 999px;
    color: var(--text-main);
    padding: 0.75rem 1rem;
    text-align: left;
    cursor: pointer;
    transition: background 0.15s ease, transform 0.15s ease;
}

.quiz-option:hover {
    background: rgba(88, 166, 255, 0.18);
    transform: translateX(2px);
}

footer {
    text-align: center;
    margin-top: 3rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--border-color);
}

footer a {
    color: var(--accent);
    text-decoration: none;
    margin: 0 1rem;
    font-weight: 500;
}

footer a:hover {
    text-decoration: underline;
}

@media (max-width: 640px) {
    body {
        padding-top: 1rem;
    }

    .card {
        padding: 1.25rem;
    }

    header h1 {
        font-size: 2rem;
    }
}

