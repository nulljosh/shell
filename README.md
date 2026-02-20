# Build Your Own Shell

A Unix shell built from scratch — command parsing, execution, piping, and job control.

## Scope
- REPL with prompt and line editing
- Command parsing and execution (fork/exec)
- Pipes (`|`) and redirects (`>`, `<`, `>>`)
- Environment variables and expansion
- Built-ins: `cd`, `exit`, `export`, `history`
- Job control (`&`, `fg`, `bg`) — stretch goal

## Learning Goals
- Process creation (fork/exec/wait)
- File descriptors and I/O redirection
- Signal handling
- Lexing and parsing command syntax
- How your terminal actually works

## Project Map

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 340" width="680" height="340" style="font-family:monospace;background:#f8fafc;border-radius:12px">
  <rect width="680" height="340" rx="12" fill="#f8fafc"/>
  <text x="340" y="28" text-anchor="middle" font-size="13" font-weight="bold" fill="#1e293b">Shell — Unix Shell from Scratch</text>
  <rect x="265" y="44" width="150" height="32" rx="6" fill="#0071e3" opacity="0.9"/>
  <text x="340" y="65" text-anchor="middle" font-size="11" fill="white" font-weight="bold">shell/ (root)</text>
  <rect x="100" y="118" width="80" height="28" rx="5" fill="#6366f1" opacity="0.85"/>
  <text x="140" y="136" text-anchor="middle" font-size="10" fill="white">src/</text>
  <rect x="220" y="118" width="90" height="28" rx="5" fill="#dcfce7" stroke="#86efac" stroke-width="1"/>
  <text x="265" y="136" text-anchor="middle" font-size="10" fill="#166534">CLAUDE.md</text>
  <rect x="330" y="118" width="90" height="28" rx="5" fill="#dcfce7" stroke="#86efac" stroke-width="1"/>
  <text x="375" y="136" text-anchor="middle" font-size="10" fill="#166534">README.md</text>
  <rect x="440" y="118" width="80" height="28" rx="5" fill="#e0f2fe" stroke="#7dd3fc" stroke-width="1"/>
  <text x="480" y="136" text-anchor="middle" font-size="10" fill="#0369a1">setup.md</text>
  <line x1="340" y1="76" x2="140" y2="118" stroke="#94a3b8" stroke-width="1" stroke-dasharray="4,2"/>
  <line x1="340" y1="76" x2="265" y2="118" stroke="#94a3b8" stroke-width="1" stroke-dasharray="4,2"/>
  <line x1="340" y1="76" x2="375" y2="118" stroke="#94a3b8" stroke-width="1" stroke-dasharray="4,2"/>
  <line x1="340" y1="76" x2="480" y2="118" stroke="#94a3b8" stroke-width="1" stroke-dasharray="4,2"/>
  <rect x="40" y="190" width="80" height="28" rx="5" fill="#e0e7ff" stroke="#818cf8" stroke-width="1"/>
  <text x="80" y="208" text-anchor="middle" font-size="10" fill="#3730a3">shell.py</text>
  <rect x="140" y="190" width="80" height="28" rx="5" fill="#e0e7ff" stroke="#818cf8" stroke-width="1"/>
  <text x="180" y="208" text-anchor="middle" font-size="10" fill="#3730a3">parser.py</text>
  <rect x="240" y="190" width="80" height="28" rx="5" fill="#e0e7ff" stroke="#818cf8" stroke-width="1"/>
  <text x="280" y="208" text-anchor="middle" font-size="10" fill="#3730a3">builtins.py</text>
  <rect x="340" y="190" width="80" height="28" rx="5" fill="#e0e7ff" stroke="#818cf8" stroke-width="1"/>
  <text x="380" y="208" text-anchor="middle" font-size="10" fill="#3730a3">exec.py</text>
  <line x1="140" y1="146" x2="80" y2="190" stroke="#818cf8" stroke-width="1.5"/>
  <line x1="140" y1="146" x2="180" y2="190" stroke="#818cf8" stroke-width="1.5"/>
  <line x1="140" y1="146" x2="280" y2="190" stroke="#818cf8" stroke-width="1.5"/>
  <line x1="140" y1="146" x2="380" y2="190" stroke="#818cf8" stroke-width="1.5"/>
  <rect x="80" y="270" width="520" height="28" rx="5" fill="#fef3c7" stroke="#fbbf24" stroke-width="1"/>
  <text x="340" y="288" text-anchor="middle" font-size="10" fill="#92400e">Unix shell from scratch — pipes, redirects, builtins, job control</text>
</svg>
```
