<div align="center">

<pre>
╔═════════════════════════════════════════════════════════════╗
║             _____  ___   _   ___   ____   _____             ║
║            /  ___|/ _ \ | \ | \ \ / /  | |  _  |            ║
║            \ `--./ /_\ \|  \| |\ V /`| |  \ V /             ║
║             `--. \  _  || . ` | \ /  | |  / _ \             ║
║            /\__/ / | | || |\  | | | _| |_| |_| |            ║
║            \____/\_| |_/\_| \_/ \_/ \___/\_____/            ║
║                                                             ║
║            hoxz :: frontend engineer :: est. 2018           ║
╠═════════════════════════════════════════════════════════════╣
║                                                             ║
║ [1] <a href="https://sany18.github.io/note-keeper/">note keeper</a> ..... secure notes, powered by google drive ║
║ [2] <a href="https://sany18.github.io/cv/">my cv</a> ........... professional journey & skills         ║
║ [3] <a href="https://alter-space.biz.ua/gta-vc/">GTA VC</a> ........... old good GTA Vice City web port      ║
║ [4] <a href="https://alter-space.biz.ua/">alter space</a> ..... web sketches, early creative work     ║
║ [5] <a href="https://hoxzy.blogspot.com/">hoxzy blog</a> ...... tech thoughts, free form              ║
║ [6] <a href="https://donatello.to/hoxz">support</a> ......... buy me a coffee                       ║
║                                                             ║
╠═════════════════════════════════════════════════════════════╣
║                      github.com/Sany18                      ║
╚═════════════════════════════════════════════════════════════╝
</pre>

</div>


---

## HTML Test

<details>
<summary>Click to expand details</summary>
<p>This is inside a details/summary block.</p>
</details>

<table>
  <tr>
    <th>Language</th>
    <th>Status</th>
  </tr>
  <tr>
    <td>HTML</td>
    <td>✅ Works</td>
  </tr>
  <tr>
    <td>CSS</td>
    <td>✅ Inline styles work</td>
  </tr>
</table>

<img src="https://via.placeholder.com/150" width="100" alt="test image" />

<span style="color:red; font-weight:bold;">Red bold text via inline style</span>

<div style="background:#222; color:#0f0; padding:10px; font-family:monospace;">
  Styled div block
</div>

<kbd>Ctrl</kbd> + <kbd>C</kbd>

<sup>superscript</sup> and <sub>subscript</sub>

<abbr title="Hypertext Markup Language">HTML</abbr>

---

## SVG CSS Animation Test

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 700 220" width="700" height="220">
  <foreignObject width="100%" height="100%">
    <div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
          font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
          background: #0d1117;
          color: #c9d1d9;
          display: flex;
          flex-direction: column;
          gap: 16px;
          padding: 20px;
        }

        h3 { color: #58a6ff; font-size: 14px; margin-bottom: 4px; }

        .row { display: flex; gap: 16px; align-items: center; }

        /* --- keyframes animation --- */
        @keyframes spin {
          from { transform: rotate(0deg); }
          to { transform: rotate(360deg); }
        }
        @keyframes bounce {
          0%, 100% { transform: translateY(0); }
          50% { transform: translateY(-12px); }
        }
        @keyframes pulse {
          0%, 100% { opacity: 1; transform: scale(1); }
          50% { opacity: 0.5; transform: scale(0.85); }
        }
        @keyframes gradient {
          0% { background-position: 0% 50%; }
          50% { background-position: 100% 50%; }
          100% { background-position: 0% 50%; }
        }

        .demo-box {
          width: 80px; height: 80px;
          border-radius: 12px;
          display: flex; align-items: center; justify-content: center;
          font-size: 28px;
          flex-shrink: 0;
        }

        .spin    { animation: spin 2s linear infinite; background: #1f6feb; }
        .bounce  { animation: bounce 1s ease-in-out infinite; background: #238636; }
        .pulse   { animation: pulse 1.5s ease-in-out infinite; background: #8957e5; }

        .gradient-box {
          width: 80px; height: 80px; border-radius: 12px;
          background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
          background-size: 400% 400%;
          animation: gradient 4s ease infinite;
          display: flex; align-items: center; justify-content: center;
          font-size: 28px; flex-shrink: 0;
        }

        /* --- hover effects --- */
        .hover-card {
          background: #161b22;
          border: 1px solid #30363d;
          border-radius: 8px;
          padding: 10px 16px;
          cursor: pointer;
          transition: all 0.3s ease;
          font-size: 13px;
          display: inline-block;
          text-decoration: none;
          color: #c9d1d9;
        }
        .hover-card:hover {
          background: #58a6ff;
          color: #0d1117;
          border-color: #58a6ff;
          transform: translateY(-3px);
          box-shadow: 0 4px 12px rgba(88, 166, 255, 0.4);
        }

        .hover-scale {
          font-size: 32px;
          transition: transform 0.2s ease;
          cursor: pointer;
          display: inline-block;
        }
        .hover-scale:hover { transform: scale(1.5) rotate(15deg); }

        .hover-glow {
          padding: 6px 14px;
          border-radius: 20px;
          border: 2px solid #f78166;
          font-size: 12px;
          color: #f78166;
          cursor: pointer;
          transition: all 0.3s ease;
          display: inline-block;
        }
        .hover-glow:hover {
          background: #f78166;
          color: #0d1117;
          box-shadow: 0 0 20px rgba(247, 129, 102, 0.6);
        }

        .labels { font-size: 11px; color: #8b949e; }

        @media (prefers-color-scheme: light) {
          body { background: #ffffff; color: #24292f; }
          .hover-card { background: #f6f8fa; border-color: #d0d7de; color: #24292f; }
          .hover-card:hover { background: #0969da; color: #fff; border-color: #0969da; }
          .hover-glow { border-color: #cf222e; color: #cf222e; }
          .hover-glow:hover { background: #cf222e; color: #fff; }
          .labels { color: #57606a; }
        }
      </style>

      <body>
        <h3>CSS Animations (@keyframes)</h3>
        <div class="row">
          <div class="demo-box spin">⚙️</div>
          <div class="demo-box bounce">🚀</div>
          <div class="demo-box pulse">💜</div>
          <div class="demo-box gradient-box">🌈</div>
          <span class="labels">spin / bounce / pulse / gradient</span>
        </div>

        <h3>Hover Effects (:hover)</h3>
        <div class="row">
          <span class="hover-card">Hover me — card lift</span>
          <span class="hover-scale">😎</span>
          <span class="hover-glow">Hover — glow ring</span>
        </div>
      </body>
    </div>
  </foreignObject>
</svg>

> If you see **animated icons** and **hover effects** above, SVG+CSS works. If it's a broken image — GitHub stripped it.
