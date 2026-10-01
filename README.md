<p align="center">
  <img src="./assets/banner.png" width="100%" alt="Tungarix. Arda, engineer in progress. Build things. Learn from them. Make the next one better. The Tungarix wolf mascot in a red jacket, sitting on a rooftop at night with a guitar.">
</p>

<p align="center">
  <a href="https://github.com/tungarix/takvim"><b>Takvim</b></a> &nbsp; / &nbsp;
  <a href="https://github.com/tungarix/habit-tracker"><b>Habit Tracker</b></a> &nbsp; / &nbsp;
  <a href="https://aktenak-site.ardaakg36.workers.dev/en/"><b>Aktenak</b></a> &nbsp; / &nbsp;
  <a href="https://x.com/tungarix"><b>X</b></a> &nbsp; / &nbsp;
  <a href="https://github.com/tungarix/takvim/issues"><b>Feedback</b></a>
</p>

<br>

I'm **Arda**, a.k.a. **Tungarix**. I'm an Electrical & Electronics Engineering student and co-founder of **[Aktenak](https://aktenak-site.ardaakg36.workers.dev/en/)**, a two-person software studio, where I handle the code and systems side.

This is where my tools live in the open: download them, read the code, and tell me when something breaks.

## Start here

<table>
  <tr>
    <td width="25%" valign="top">
      <sub>01 / CALENDAR</sub>
      <h3><a href="https://github.com/tungarix/takvim">Takvim</a></h3>
      <p>A local-first desktop calendar. No account, no internet: your data stays on your machine.</p>
      <p><a href="https://github.com/tungarix/takvim/releases/latest"><b>Download for Windows →</b></a></p>
    </td>
    <td width="25%" valign="top">
      <sub>02 / HABITS</sub>
      <h3><a href="https://github.com/tungarix/habit-tracker">Habit Tracker</a></h3>
      <p>A local-first habit tracker. Habits, mood, tasks and focus sessions in one panel.</p>
      <p><a href="https://github.com/tungarix/habit-tracker/releases/latest"><b>Download for Windows →</b></a></p>
    </td>
    <td width="25%" valign="top">
      <sub>03 / AI</sub>
      <h3><a href="https://github.com/tungarix/yerel-llm-8gb">Local LLM setup</a></h3>
      <p>Two open-weight models on 8 GB of VRAM — measured llama.cpp flags, and a quantization finding.</p>
      <p><a href="https://github.com/tungarix/yerel-llm-8gb"><b>Read the notes →</b></a></p>
    </td>
    <td width="25%" valign="top">
      <sub>04 / STUDIO</sub>
      <h3><a href="https://aktenak-site.ardaakg36.workers.dev/en/">Aktenak</a></h3>
      <p>A two-person studio based in Kocaeli, Türkiye. Small output, high care: narrow focus over broad promises.</p>
      <p><a href="https://aktenak-site.ardaakg36.workers.dev/en/studio/"><b>Meet the studio →</b></a></p>
    </td>
  </tr>
</table>

## On the workbench: Takvim

**No account, no internet, one file.** A desktop calendar for Windows with day, week and month views, recurring events, tasks you can drop onto the calendar, reminders, and `.ics` import and export. Built with Python + pywebview; your data lives in a local SQLite file. Interface in Turkish or English.

<p align="center">
  <a href="https://github.com/tungarix/takvim">
    <img src="https://raw.githubusercontent.com/tungarix/takvim/master/docs/screenshot.png" width="100%" alt="Takvim's week view: a mini month calendar and calendar list on the left, color-coded event blocks on the right.">
  </a>
</p>

**It's looking for its first real users.** Try it and tell me what's missing or broken: [open an issue](https://github.com/tungarix/takvim/issues), or read more on the [product page](https://aktenak-site.ardaakg36.workers.dev/en/projects/takvim/).

| Topic | In short |
| :--- | :--- |
| **Data** | On your machine, in local SQLite. No account, no server. |
| **Portability** | `.ics` import and export, so you can move in from or out to other calendars. |
| **Quality** | 623 tests, CI on every push, automated releases with build attestation (GitHub Actions). |
| **License** | MIT |

<br>

## Also shipped: Habit Tracker

**No account, no server.** A desktop habit tracker: daily check-ins, a 30-day heat strip per habit, a Pomodoro focus timer, weekly tasks, mood tracking, a classic monthly grid view, and streak/completion stats — including a mood-to-completion correlation. Runs from the system tray, has keyboard shortcuts (`Ctrl+1..4` tabs, `Ctrl+N` new habit), an optional start-at-login toggle, and an evening reminder if you haven't checked in yet. Built with Flutter; your data lives in a local SQLite database.

<p align="center">
  <a href="https://github.com/tungarix/habit-tracker">
    <img src="https://raw.githubusercontent.com/tungarix/habit-tracker/master/docs/screenshot.png" width="100%" alt="Habit Tracker's daily panel: today's habits and mood picker on the left, 30-day heat strips in the middle, a focus timer and weekly tasks on the right.">
  </a>
</p>

Try it and tell me what's missing or broken: [open an issue](https://github.com/tungarix/habit-tracker/issues), or read more on the [product page](https://aktenak-site.ardaakg36.workers.dev/en/projects/habit-tracker/).

| Topic | In short |
| :--- | :--- |
| **Data** | On your machine, local SQLite. No account, no server. |
| **Backup** | Full JSON export/import — merge or replace. |
| **Platform** | Windows, portable — unzip and run. |
| **Quality** | 72 tests, CI + automated releases with GitHub Actions. |
| **License** | MIT |

<br>

## Contributions

Found and fixed two Windows installer/test bugs in [avenoxbeyin](https://github.com/avenoxai/avenoxbeyin) that broke the V2→V3 upgrade and hid 23 test failures on Python 3.14 — both merged same-day.
[#119](https://github.com/avenoxai/avenoxbeyin/pull/119) · [#126](https://github.com/avenoxai/avenoxbeyin/pull/126)

Traced two blockers that left a failed `update` unrecoverable, each reported with a full trace. The first, a Windows/MSIX deadlock, the maintainer fixed upstream in v3.6.0 and credited the report. For the second, where `recover` died on a stale checksum after a note was edited, I wrote the fix and its regression tests — merged the same day.
[#139](https://github.com/avenoxai/avenoxbeyin/issues/139) · [#162](https://github.com/avenoxai/avenoxbeyin/pull/162) · [#181](https://github.com/avenoxai/avenoxbeyin/issues/181) · [#182](https://github.com/avenoxai/avenoxbeyin/pull/182)

<br>

---

<p align="center">
  <b>BUILD · LEARN · CREATE</b><br>
  <sub>Into systems design, AI, electronics, game development and music.</sub>
</p>
