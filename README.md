# ADV-Part1a-Compliance-Application
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Form ADV Part 1A — Investment Adviser Registration</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root {
  --navy: #0f2044;
  --navy-mid: #1a3360;
  --navy-light: #2a4a80;
  --blue-soft: #eef2f9;
  --gold: #c8963e;
  --gold-light: #f0d898;
  --gold-bg: #fdf8ee;
  --green: #1a7f4b;
  --green-bg: #edfaf2;
  --red: #c0392b;
  --red-bg: #fdf1f0;
  --orange: #c25f1a;
  --orange-bg: #fef5ed;
  --purple: #6c3fc5;
  --purple-bg: #f3eefd;
  --gray-50: #f9fafb;
  --gray-100: #f3f4f6;
  --gray-200: #e5e7eb;
  --gray-300: #d1d5db;
  --gray-400: #9ca3af;
  --gray-500: #6b7280;
  --gray-600: #4b5563;
  --gray-700: #374151;
  --gray-800: #1f2937;
  --white: #ffffff;
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.08), 0 1px 2px rgba(0,0,0,0.04);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.08), 0 2px 4px rgba(0,0,0,0.04);
  --shadow-lg: 0 10px 30px rgba(0,0,0,0.1), 0 4px 10px rgba(0,0,0,0.05);
  --radius: 8px;
  --radius-sm: 5px;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { font-family: 'Inter', sans-serif; background: var(--gray-100); color: var(--gray-800); min-height: 100vh; font-size: 14px; line-height: 1.5; }

/* ═══════════════ TOP HEADER ═══════════════ */
.top-header {
  background: var(--navy);
  color: white;
  position: sticky; top: 0; z-index: 200;
  box-shadow: 0 2px 12px rgba(0,0,0,0.25);
}
.header-row1 {
  display: flex; align-items: center; justify-content: space-between;
  padding: 12px 24px; max-width: 1400px; margin: 0 auto;
}
.logo-wrap { display: flex; align-items: center; gap: 12px; }
.logo-icon {
  width: 38px; height: 38px; background: var(--gold); border-radius: 6px;
  display: flex; align-items: center; justify-content: center;
  font-weight: 700; font-size: 16px; color: var(--navy); flex-shrink: 0;
  letter-spacing: -0.5px;
}
.logo-title { font-weight: 700; font-size: 16px; line-height: 1.2; }
.logo-sub { font-size: 11px; color: rgba(255,255,255,0.5); font-weight: 400; }
.header-actions { display: flex; align-items: center; gap: 10px; }
.hdr-btn {
  display: flex; align-items: center; gap: 6px; padding: 7px 14px;
  border-radius: 6px; font-size: 13px; font-weight: 500; cursor: pointer;
  border: none; transition: all 0.15s; font-family: 'Inter', sans-serif;
}
.hdr-btn-outline { background: rgba(255,255,255,0.1); color: white; border: 1px solid rgba(255,255,255,0.2); }
.hdr-btn-outline:hover { background: rgba(255,255,255,0.18); }
.hdr-btn-gold { background: var(--gold); color: var(--navy); }
.hdr-btn-gold:hover { background: #d9a84e; }

/* Progress bar row */
.header-row2 { border-top: 1px solid rgba(255,255,255,0.1); padding: 0; }
.progress-track { height: 3px; background: rgba(255,255,255,0.1); }
.progress-fill { height: 100%; background: linear-gradient(90deg, var(--gold), #e8b84a); transition: width 0.5s ease; }

/* ═══════════════ LAYOUT ═══════════════ */
.app-shell { display: flex; max-width: 1400px; margin: 0 auto; min-height: calc(100vh - 65px); }

/* ═══════════════ SIDEBAR ═══════════════ */
.sidebar {
  width: 280px; flex-shrink: 0; background: var(--white);
  border-right: 1px solid var(--gray-200);
  position: sticky; top: 65px; height: calc(100vh - 65px);
  overflow-y: auto; display: flex; flex-direction: column;
}
.sidebar-header {
  padding: 16px 18px 12px; border-bottom: 1px solid var(--gray-100);
  flex-shrink: 0;
}
.sidebar-header h3 { font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.08em; color: var(--gray-400); }
.overall-progress { margin-top: 10px; }
.op-label { display: flex; justify-content: space-between; font-size: 12px; color: var(--gray-500); margin-bottom: 5px; }
.op-label strong { color: var(--navy); font-weight: 600; }
.op-bar { height: 6px; background: var(--gray-100); border-radius: 99px; overflow: hidden; }
.op-fill { height: 100%; background: linear-gradient(90deg, var(--navy), var(--navy-light)); border-radius: 99px; transition: width 0.4s; }

.nav-list { flex: 1; padding: 8px 0; overflow-y: auto; }
.nav-group-label {
  padding: 10px 18px 4px; font-size: 10px; font-weight: 700;
  text-transform: uppercase; letter-spacing: 0.1em; color: var(--gray-400);
}
.nav-item {
  display: flex; align-items: center; gap: 10px;
  padding: 9px 18px; cursor: pointer; transition: all 0.12s;
  border-left: 3px solid transparent; position: relative;
}
.nav-item:hover { background: var(--blue-soft); }
.nav-item.active { background: var(--blue-soft); border-left-color: var(--navy); }
.nav-item.active .nav-label { color: var(--navy); font-weight: 600; }
.nav-item.completed .nav-badge { background: var(--green); border-color: var(--green); color: white; }
.nav-item.completed .nav-label { color: var(--gray-600); }
.nav-item.has-issues .nav-badge { background: var(--red-bg); border-color: var(--red); color: var(--red); }
.nav-badge {
  width: 20px; height: 20px; border-radius: 50%; border: 1.5px solid var(--gray-300);
  display: flex; align-items: center; justify-content: center; font-size: 9px;
  font-weight: 700; flex-shrink: 0; transition: all 0.2s; color: var(--gray-400);
}
.nav-badge-num { font-family: 'IBM Plex Mono', monospace; font-size: 9px; }
.nav-label { font-size: 12.5px; color: var(--gray-600); line-height: 1.3; flex: 1; }
.nav-item-ref { font-family: 'IBM Plex Mono', monospace; font-size: 10px; color: var(--gray-400); }

.sidebar-footer {
  border-top: 1px solid var(--gray-100); padding: 14px 18px;
  flex-shrink: 0;
}
.help-card {
  background: var(--blue-soft); border-radius: var(--radius-sm);
  padding: 12px; font-size: 12px; color: var(--gray-600); line-height: 1.5;
}
.help-card strong { color: var(--navy); font-weight: 600; display: block; margin-bottom: 4px; }
.help-card a { color: var(--navy-light); text-decoration: none; font-weight: 500; }
.sidebar::-webkit-scrollbar { width: 4px; }
.sidebar::-webkit-scrollbar-thumb { background: var(--gray-200); border-radius: 2px; }

/* ═══════════════ MAIN CONTENT ═══════════════ */
.main-content { flex: 1; padding: 28px 36px; overflow-y: auto; min-width: 0; max-width: 900px; }

/* ═══════════════ SECTION SHELL ═══════════════ */
.form-section { display: none; animation: fadeUp 0.2s ease; }
.form-section.active { display: block; }
@keyframes fadeUp { from { opacity: 0; transform: translateY(8px); } to { opacity: 1; transform: translateY(0); } }

/* Section header */
.section-hd {
  display: flex; align-items: flex-start; justify-content: space-between;
  margin-bottom: 24px; padding-bottom: 20px; border-bottom: 2px solid var(--gray-200);
  gap: 16px;
}
.section-hd-left { flex: 1; }
.section-eyebrow {
  display: flex; align-items: center; gap: 8px; margin-bottom: 6px;
}
.eyebrow-tag {
  font-family: 'IBM Plex Mono', monospace; font-size: 10px; font-weight: 500;
  color: var(--navy); background: var(--blue-soft); padding: 2px 8px;
  border-radius: 99px; border: 1px solid rgba(15,32,68,0.12);
}
.section-title { font-size: 22px; font-weight: 700; color: var(--navy); line-height: 1.2; margin-bottom: 6px; }
.section-subtitle { font-size: 13px; color: var(--gray-500); line-height: 1.6; max-width: 620px; }
.section-completion {
  display: flex; flex-direction: column; align-items: flex-end; gap: 4px; flex-shrink: 0;
}
.completion-pct { font-size: 22px; font-weight: 700; color: var(--navy); font-family: 'IBM Plex Mono', monospace; }
.completion-label { font-size: 11px; color: var(--gray-400); }

/* ═══════════════ SUBSECTIONS ═══════════════ */
.subsection {
  background: var(--white); border: 1px solid var(--gray-200); border-radius: var(--radius);
  margin-bottom: 16px; overflow: hidden; box-shadow: var(--shadow-sm);
}
.subsection-header {
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px 20px; cursor: pointer; user-select: none;
  border-bottom: 1px solid var(--gray-100); transition: background 0.1s;
}
.subsection-header:hover { background: var(--gray-50); }
.subsection-header.collapsed { border-bottom: none; }
.ss-left { display: flex; align-items: center; gap: 10px; }
.ss-badge {
  font-family: 'IBM Plex Mono', monospace; font-size: 10px; font-weight: 600;
  color: var(--gold); background: var(--gold-bg); border: 1px solid rgba(200,150,62,0.25);
  padding: 2px 8px; border-radius: 99px; flex-shrink: 0;
}
.ss-title { font-size: 14px; font-weight: 600; color: var(--gray-800); }
.ss-right { display: flex; align-items: center; gap: 10px; }
.ss-status { font-size: 11px; color: var(--gray-400); font-weight: 500; }
.ss-chevron { color: var(--gray-400); transition: transform 0.2s; font-size: 12px; }
.subsection-header.collapsed .ss-chevron { transform: rotate(-90deg); }
.subsection-body { padding: 20px; display: block; }
.subsection-body.hidden { display: none; }

/* ═══════════════ FORM GRID ═══════════════ */
.fg { display: grid; gap: 16px; }
.fg-2 { grid-template-columns: 1fr 1fr; }
.fg-3 { grid-template-columns: 1fr 1fr 1fr; }
.fg-4 { grid-template-columns: 1fr 1fr 1fr 1fr; }
.gc-full { grid-column: 1 / -1; }
.gc-2 { grid-column: span 2; }
.fg + .fg { margin-top: 16px; }

/* ═══════════════ FORM FIELDS ═══════════════ */
.field { display: flex; flex-direction: column; gap: 5px; }
.field-lbl {
  font-size: 12.5px; font-weight: 600; color: var(--gray-700);
  display: flex; align-items: flex-start; gap: 5px; flex-wrap: wrap; line-height: 1.4;
}
.field-lbl .req { color: var(--red); flex-shrink: 0; line-height: 1.4; }
.field-ref {
  font-family: 'IBM Plex Mono', monospace; font-size: 10px; color: var(--gray-400);
  background: var(--gray-100); padding: 1px 6px; border-radius: 99px; white-space: nowrap;
}
.field-hint { font-size: 11.5px; color: var(--gray-500); line-height: 1.5; }
.field-error { font-size: 11.5px; color: var(--red); display: none; }
.field.errored .field-error { display: block; }
.field.errored input, .field.errored select, .field.errored textarea { border-color: var(--red) !important; }

/* Tooltip */
.tip-icon {
  display: inline-flex; align-items: center; justify-content: center;
  width: 15px; height: 15px; border-radius: 50%; background: var(--gray-200);
  color: var(--gray-500); font-size: 10px; font-weight: 700; cursor: help;
  position: relative; flex-shrink: 0;
}
.tip-icon:hover::after {
  content: attr(data-tip);
  position: absolute; bottom: calc(100% + 6px); left: 50%; transform: translateX(-50%);
  background: var(--gray-800); color: white; font-size: 11.5px; font-weight: 400;
  padding: 7px 10px; border-radius: 6px; white-space: normal; width: 260px;
  z-index: 9999; box-shadow: var(--shadow-md); line-height: 1.5;
  pointer-events: none;
}
.tip-icon:hover::before {
  content: ''; position: absolute; bottom: calc(100% + 1px); left: 50%; transform: translateX(-50%);
  border: 5px solid transparent; border-top-color: var(--gray-800); z-index: 9999;
}

/* Inputs */
input[type="text"], input[type="email"], input[type="tel"], input[type="number"],
input[type="date"], input[type="url"], select, textarea {
  width: 100%; padding: 9px 12px; border: 1.5px solid var(--gray-300);
  border-radius: 6px; font-family: 'Inter', sans-serif; font-size: 13.5px;
  color: var(--gray-800); background: var(--white); transition: all 0.12s; outline: none;
  appearance: none;
}
input:hover, select:hover, textarea:hover { border-color: var(--gray-400); }
input:focus, select:focus, textarea:focus {
  border-color: var(--navy); box-shadow: 0 0 0 3px rgba(15,32,68,0.08);
}
input::placeholder { color: var(--gray-400); }
textarea { resize: vertical; min-height: 80px; line-height: 1.6; }
select {
  cursor: pointer;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6' viewBox='0 0 10 6'%3E%3Cpath d='M1 1l4 4 4-4' stroke='%236b7280' stroke-width='1.5' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E");
  background-repeat: no-repeat; background-position: right 12px center; padding-right: 34px;
}
input[type="number"] { -moz-appearance: textfield; }
input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button { -webkit-appearance: none; }

.input-addon { display: flex; }
.input-addon input { border-radius: 6px 0 0 6px; border-right: 0; }
.input-addon input:focus { border-right: 1.5px solid var(--navy); border-radius: 6px 0 0 6px; }
.addon-after {
  background: var(--gray-100); border: 1.5px solid var(--gray-300); border-left: 0;
  border-radius: 0 6px 6px 0; padding: 9px 12px; font-size: 13px; color: var(--gray-500);
  white-space: nowrap; display: flex; align-items: center;
}

/* Character counter */
.input-with-count { position: relative; }
.char-count { position: absolute; right: 10px; bottom: 8px; font-size: 10px; color: var(--gray-400); pointer-events: none; }

/* ═══════════════ YES/NO TOGGLE ═══════════════ */
.yn-toggle { display: flex; gap: 6px; }
.yn-btn {
  flex: 1; padding: 8px 0; text-align: center; border: 1.5px solid var(--gray-300);
  border-radius: 6px; font-size: 13px; font-weight: 500; cursor: pointer;
  transition: all 0.15s; background: var(--white); color: var(--gray-600);
  user-select: none;
}
.yn-btn.yn-yes:hover { border-color: var(--green); color: var(--green); background: var(--green-bg); }
.yn-btn.yn-no:hover { border-color: var(--red); color: var(--red); background: var(--red-bg); }
.yn-btn.sel-yes { border-color: var(--green); color: var(--green); background: var(--green-bg); font-weight: 600; }
.yn-btn.sel-no { border-color: var(--red); color: var(--red); background: var(--red-bg); font-weight: 600; }
.yn-hidden { display: none; }

/* ═══════════════ CHECK / RADIO OPTIONS ═══════════════ */
.opt-list { display: flex; flex-direction: column; gap: 6px; }
.opt-list.inline { flex-direction: row; flex-wrap: wrap; gap: 6px; }
.opt-item {
  display: flex; align-items: flex-start; gap: 10px; padding: 9px 13px;
  border: 1.5px solid var(--gray-200); border-radius: 6px; background: var(--white);
  cursor: pointer; transition: all 0.12s; font-size: 13px; color: var(--gray-700);
  line-height: 1.45;
}
.opt-item:hover { border-color: var(--gray-400); background: var(--gray-50); }
.opt-item input { width: auto !important; margin-top: 2px; flex-shrink: 0; accent-color: var(--navy); cursor: pointer; }
.opt-item.sel { border-color: var(--navy); background: var(--blue-soft); color: var(--navy); }
.opt-item.sel-warn { border-color: var(--red); background: var(--red-bg); color: var(--gray-800); }

/* ═══════════════ STATE PICKER ═══════════════ */
.state-picker { position: relative; }
.state-search { margin-bottom: 8px; }
.state-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(52px, 1fr)); gap: 4px; max-height: 200px; overflow-y: auto; border: 1px solid var(--gray-200); border-radius: 6px; padding: 8px; background: var(--gray-50); }
.state-chip {
  padding: 4px 6px; border: 1.5px solid var(--gray-200); border-radius: 4px;
  background: var(--white); font-size: 12px; font-weight: 500; cursor: pointer;
  text-align: center; transition: all 0.1s; color: var(--gray-600);
}
.state-chip:hover { border-color: var(--navy-light); }
.state-chip.sel { border-color: var(--navy); background: var(--navy); color: white; }
.state-chip input { display: none; }
.state-actions { display: flex; gap: 8px; margin-bottom: 8px; }
.state-act-btn {
  font-size: 12px; padding: 4px 10px; border: 1px solid var(--gray-300);
  border-radius: 4px; background: var(--white); cursor: pointer; color: var(--gray-600);
  transition: all 0.12s;
}
.state-act-btn:hover { background: var(--gray-100); }
.selected-states-summary { font-size: 12px; color: var(--gray-500); margin-top: 6px; }
.selected-states-summary strong { color: var(--navy); }

/* ═══════════════ CONDITIONAL REVEAL ═══════════════ */
.conditional { display: none; }
.conditional.show { display: block; }
.cond-indent {
  margin-top: 12px; padding: 14px 16px; border-left: 3px solid var(--gold);
  background: var(--gold-bg); border-radius: 0 6px 6px 0;
}
.cond-indent .fg, .cond-indent .fg-2 { margin-top: 0; }

/* ═══════════════ DISC ROWS (Item 11) ═══════════════ */
.disc-row {
  display: grid; grid-template-columns: 1fr auto; gap: 16px; align-items: center;
  padding: 13px 16px; border: 1.5px solid var(--gray-200); border-radius: 6px;
  background: var(--white); margin-bottom: 6px; transition: border-color 0.15s;
}
.disc-row:hover { border-color: var(--gray-300); }
.disc-row.disc-yes { border-color: var(--red); background: var(--red-bg); }
.disc-row p { font-size: 13px; color: var(--gray-700); line-height: 1.5; }
.disc-yn { flex-shrink: 0; min-width: 130px; }

/* ═══════════════ SCHEDULE TABLE ═══════════════ */
.sched-table-wrap { overflow-x: auto; border-radius: 6px; border: 1px solid var(--gray-200); }
table.sched-table { width: 100%; border-collapse: collapse; font-size: 13px; }
table.sched-table th {
  background: var(--navy); color: white; padding: 10px 12px;
  text-align: left; font-weight: 500; font-size: 12px; white-space: nowrap;
}
table.sched-table td { padding: 8px 10px; border-bottom: 1px solid var(--gray-100); vertical-align: middle; }
table.sched-table tr:last-child td { border-bottom: none; }
table.sched-table tr:hover td { background: var(--gray-50); }
table.sched-table input, table.sched-table select { padding: 6px 10px; font-size: 13px; border-radius: 4px; }

/* ═══════════════ ENTRY CARDS ═══════════════ */
.entry-card {
  border: 1.5px solid var(--gray-200); border-radius: var(--radius);
  background: var(--white); margin-bottom: 10px; overflow: hidden;
  box-shadow: var(--shadow-sm);
}
.entry-card-hd {
  display: flex; align-items: center; justify-content: space-between;
  padding: 10px 16px; background: var(--gray-50); border-bottom: 1px solid var(--gray-200);
}
.entry-card-hd span { font-size: 13px; font-weight: 600; color: var(--gray-700); }
.entry-card-actions { display: flex; gap: 6px; align-items: center; }
.entry-del {
  background: none; border: 1px solid var(--red); color: var(--red); border-radius: 4px;
  padding: 3px 9px; font-size: 12px; cursor: pointer; transition: all 0.15s;
}
.entry-del:hover { background: var(--red); color: white; }
.entry-body { padding: 18px; }
.btn-add-entry {
  display: flex; align-items: center; justify-content: center; gap: 8px;
  width: 100%; padding: 10px; border: 2px dashed var(--gray-300); border-radius: 6px;
  background: transparent; color: var(--gray-500); font-size: 13px; font-weight: 500;
  cursor: pointer; transition: all 0.15s; font-family: 'Inter', sans-serif; margin-top: 6px;
}
.btn-add-entry:hover { border-color: var(--navy); color: var(--navy); background: var(--blue-soft); }

/* ═══════════════ ALERT / INFO BOXES ═══════════════ */
.alert {
  display: flex; gap: 12px; padding: 12px 16px; border-radius: var(--radius-sm);
  font-size: 13px; line-height: 1.55; margin-bottom: 16px;
}
.alert-icon { font-size: 16px; flex-shrink: 0; margin-top: 1px; }
.alert-body strong { font-weight: 600; display: block; margin-bottom: 2px; }
.alert-info { background: var(--blue-soft); border: 1px solid rgba(15,32,68,0.12); color: var(--navy-mid); }
.alert-warn { background: var(--orange-bg); border: 1px solid rgba(194,95,26,0.2); color: var(--orange); }
.alert-error { background: var(--red-bg); border: 1px solid rgba(192,57,43,0.2); color: var(--red); }
.alert-success { background: var(--green-bg); border: 1px solid rgba(26,127,75,0.2); color: var(--green); }
.alert-purple { background: var(--purple-bg); border: 1px solid rgba(108,63,197,0.2); color: var(--purple); }

/* ═══════════════ RULE CITE ═══════════════ */
.rule-cite {
  display: inline-flex; align-items: center; gap: 4px; padding: 2px 7px;
  background: var(--purple-bg); border: 1px solid rgba(108,63,197,0.2);
  border-radius: 99px; font-size: 11px; color: var(--purple); font-weight: 500;
  font-family: 'IBM Plex Mono', monospace; white-space: nowrap;
}

/* ═══════════════ DRP NOTICE ═══════════════ */
.drp-notice {
  display: none; margin-top: 8px; padding: 8px 12px; background: var(--red-bg);
  border: 1px solid rgba(192,57,43,0.25); border-radius: 5px;
  font-size: 12px; color: var(--red); line-height: 1.5;
}
.drp-notice.show { display: block; }

/* ═══════════════ SECTION NAV ═══════════════ */
.section-nav {
  display: flex; align-items: center; justify-content: space-between;
  margin-top: 36px; padding-top: 20px; border-top: 2px solid var(--gray-200);
}
.nav-btn {
  display: flex; align-items: center; gap: 8px; padding: 10px 22px;
  border-radius: 7px; font-size: 14px; font-weight: 600; cursor: pointer;
  transition: all 0.15s; border: none; font-family: 'Inter', sans-serif;
}
.nav-btn-back { background: var(--white); color: var(--gray-700); border: 1.5px solid var(--gray-300); }
.nav-btn-back:hover { border-color: var(--navy); color: var(--navy); }
.nav-btn-next { background: var(--navy); color: white; }
.nav-btn-next:hover { background: var(--navy-mid); }
.nav-btn-submit { background: var(--gold); color: var(--navy); }
.nav-btn-submit:hover { background: #d9a84e; }
.nav-section-info { text-align: center; }
.nav-section-num { font-size: 12px; color: var(--gray-400); font-family: 'IBM Plex Mono', monospace; }
.nav-section-name { font-size: 12px; color: var(--gray-600); font-weight: 500; }

/* ═══════════════ SUCCESS SCREEN ═══════════════ */
.success-wrap { text-align: center; padding: 60px 20px; }
.success-icon-big {
  width: 80px; height: 80px; background: var(--green); border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-size: 36px; margin: 0 auto 24px; box-shadow: 0 0 0 12px rgba(26,127,75,0.12);
}
.success-wrap h2 { font-size: 28px; font-weight: 700; color: var(--navy); margin-bottom: 12px; }
.success-wrap p { font-size: 14px; color: var(--gray-500); max-width: 520px; margin: 0 auto 8px; line-height: 1.7; }
.success-actions { display: flex; gap: 12px; justify-content: center; margin-top: 28px; flex-wrap: wrap; }
.success-checklist {
  max-width: 480px; margin: 20px auto 0; background: var(--blue-soft);
  border: 1px solid rgba(15,32,68,0.1); border-radius: var(--radius);
  padding: 16px 20px; text-align: left;
}
.success-checklist h4 { font-size: 13px; font-weight: 700; color: var(--navy); margin-bottom: 10px; }
.success-checklist li { font-size: 12.5px; color: var(--gray-700); padding: 4px 0; padding-left: 18px; position: relative; line-height: 1.5; }
.success-checklist li::before { content: '✓'; position: absolute; left: 0; color: var(--green); font-weight: 700; }

/* ═══════════════ DIVIDER ═══════════════ */
.divider { border: none; border-top: 1px solid var(--gray-200); margin: 18px 0; }

/* ═══════════════ TAG PILL ═══════════════ */
.tag-pill {
  display: inline-flex; align-items: center; gap: 4px; padding: 2px 8px;
  border-radius: 99px; font-size: 11px; font-weight: 500;
}
.tag-optional { background: var(--gray-100); color: var(--gray-500); }
.tag-required { background: rgba(192,57,43,0.08); color: var(--red); }
.tag-new { background: rgba(108,63,197,0.1); color: var(--purple); }

/* ═══════════════ CERTIFICATION BOX ═══════════════ */
.cert-box {
  border: 2px solid var(--gray-300); border-radius: var(--radius);
  padding: 20px; transition: border-color 0.2s;
}
.cert-box.cert-signed { border-color: var(--green); background: var(--green-bg); }
.cert-text { font-size: 13px; color: var(--gray-700); line-height: 1.7; font-style: italic; margin-bottom: 16px; }
.cert-check-row { display: flex; align-items: flex-start; gap: 10px; cursor: pointer; }
.cert-check-row input { width: auto !important; margin-top: 2px; accent-color: var(--green); }
.cert-check-label { font-size: 13px; font-weight: 600; color: var(--gray-800); line-height: 1.5; }

/* ═══════════════ MOBILE ═══════════════ */
@media (max-width: 960px) {
  .sidebar { display: none; }
  .main-content { padding: 18px 16px; }
  .fg-2, .fg-3, .fg-4 { grid-template-columns: 1fr; }
  .gc-full, .gc-2 { grid-column: 1; }
  .section-hd { flex-direction: column; }
}
</style>
</head>
<body>

<!-- TOP HEADER -->
<header class="top-header">
  <div class="header-row1">
    <div class="logo-wrap">
      <div class="logo-icon">ADV</div>
      <div>
        <div class="logo-title">Form ADV Part 1A</div>
        <div class="logo-sub">SEC Investment Adviser Registration System</div>
      </div>
    </div>
    <div class="header-actions">
      <button class="hdr-btn hdr-btn-outline" onclick="exportSummary()">⬇ Export Summary</button>
      <button class="hdr-btn hdr-btn-outline" onclick="saveProgress()">💾 Save Draft</button>
      <button class="hdr-btn hdr-btn-gold" onclick="showHelp()">? Help</button>
    </div>
  </div>
  <div class="header-row2">
    <div class="progress-track"><div class="progress-fill" id="pgbar" style="width:0%"></div></div>
  </div>
</header>

<div class="app-shell">

  <!-- SIDEBAR -->
  <aside class="sidebar">
    <div class="sidebar-header">
      <h3>Filing Progress</h3>
      <div class="overall-progress">
        <div class="op-label"><span>Overall completion</span><strong id="pct-label">0%</strong></div>
        <div class="op-bar"><div class="op-fill" id="overall-fill" style="width:0%"></div></div>
      </div>
    </div>
    <div class="nav-list" id="nav-list"></div>
    <div class="sidebar-footer">
      <div class="help-card">
        <strong>📋 Filing Resources</strong>
        File via IARD at <a href="https://www.iard.com" target="_blank">iard.com</a>. For instructions, visit <a href="https://www.sec.gov/info/edgar/siccodes.htm" target="_blank">SEC.gov</a>. DRPs required for all "Yes" disclosures.
      </div>
    </div>
  </aside>

  <!-- MAIN -->
  <main class="main-content" id="main-content"></main>
</div>

<script>
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// CONSTANTS & STATE
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
const STATES = ['AL','AK','AZ','AR','CA','CO','CT','DE','DC','FL','GA','GU','HI','ID','IL','IN','IA','KS','KY','LA','ME','MD','MA','MI','MN','MS','MO','MT','NE','NV','NH','NJ','NM','NY','NC','ND','OH','OK','OR','PA','PR','RI','SC','SD','TN','TX','UT','VT','VI','VA','WA','WV','WI','WY'];
let currentIdx = 0;
let entryCounters = {};
let sectionCompletion = {};

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// HTML BUILDER HELPERS
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
function field(label, ref, input, hint, req, tip, optional) {
  const reqHtml = req ? '<span class="req">*</span>' : '';
  const refHtml = ref ? `<span class="field-ref">${ref}</span>` : '';
  const tipHtml = tip ? `<span class="tip-icon" data-tip="${tip}">?</span>` : '';
  const optHtml = optional ? '<span class="tag-pill tag-optional">optional</span>' : '';
  const hintHtml = hint ? `<div class="field-hint">${hint}</div>` : '';
  return `<div class="field">
    <label class="field-lbl">${label}${reqHtml}${refHtml}${tipHtml}${optHtml}</label>
    ${input}
    ${hintHtml}
    <div class="field-error">This field is required</div>
  </div>`;
}
function inp(type, ph, extra='') { return `<input type="${type}" placeholder="${ph||''}" ${extra}>`; }
function sel(opts, ph='Select') {
  return `<select><option value="">— ${ph} —</option>${opts.map(o=>Array.isArray(o)?`<option value="${o[0]}">${o[1]}</option>`:`<option>${o}</option>`).join('')}</select>`;
}
function addon(inputHtml, suffix) {
  return `<div class="input-addon">${inputHtml}<span class="addon-after">${suffix}</span></div>`;
}
function yn(name, compact=false) {
  return `<div class="yn-toggle">
    <div class="yn-btn yn-yes" data-name="${name}" data-val="yes" onclick="setYN(this)">✓ Yes</div>
    <div class="yn-btn yn-no" data-name="${name}" data-val="no" onclick="setYN(this)">✗ No</div>
    <input type="hidden" name="${name}" value="" class="yn-hidden">
  </div>`;
}
function discRow(label, name, drpType) {
  const drp = drpType ? `<div class="drp-notice" id="drp-${name}">⚠️ A <strong>${drpType}</strong> Disclosure Reporting Page (DRP) is required for this disclosure. Complete it in IARD after submitting this form.</div>` : '';
  return `<div class="disc-row" id="drow-${name}">
    <div><p>${label}</p>${drp}</div>
    <div class="disc-yn">${yn(name)}</div>
  </div>`;
}
function alert_(type, icon, title, body) {
  return `<div class="alert alert-${type}"><div class="alert-icon">${icon}</div><div class="alert-body"><strong>${title}</strong>${body}</div></div>`;
}
function stateGrid(name) {
  const chips = STATES.map(s=>`<label class="state-chip" onclick="toggleState(this,'${name}','${s}')"><input type="checkbox" name="${name}" value="${s}" style="display:none">${s}</label>`).join('');
  return `<div class="state-picker">
    <div class="state-actions">
      <button class="state-act-btn" onclick="toggleAllStates('${name}',true)">Select All</button>
      <button class="state-act-btn" onclick="toggleAllStates('${name}',false)">Clear All</button>
    </div>
    <input type="text" placeholder="🔍 Filter states…" class="state-search" oninput="filterStates(this,'${name}')">
    <div class="state-grid" id="sg-${name}">${chips}</div>
    <div class="selected-states-summary" id="ss-${name}">No states selected</div>
  </div>`;
}
function cond(id, content) {
  return `<div class="conditional cond-indent" id="cond-${id}">${content}</div>`;
}
function sub(badge, title, body, id='') {
  const sid = id || badge.replace(/[^a-z0-9]/gi,'_');
  return `<div class="subsection">
    <div class="subsection-header" onclick="toggleSub(this)" id="ssh-${sid}">
      <div class="ss-left">
        <span class="ss-badge">${badge}</span>
        <span class="ss-title">${title}</span>
      </div>
      <div class="ss-right">
        <span class="ss-status" id="ss-stat-${sid}"></span>
        <span class="ss-chevron">▼</span>
      </div>
    </div>
    <div class="subsection-body" id="ss-body-${sid}">${body}</div>
  </div>`;
}

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// SECTIONS DATA
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
const SECTIONS = [

// ─────────────── SECTION 0: FILING TYPE ───────────────
{ id:'filing-type', short:'Filing Type', item:'Filing Setup', title:'Filing Type & Purpose',
  subtitle:'Tell us what kind of filing this is before we begin. This helps customize which fields apply to your situation.',
  icon:'📋',
  html:`
${sub('Setup','What Would You Like to Do?',`
  ${alert_('info','📋','Select all that apply','Check every box that describes this submission. Your selections will determine which sections are required.')}
  <div class="opt-list">
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Initial SEC Registration</strong><br><span style="font-size:12px;color:var(--gray-500)">First-time application to register as an investment adviser with the SEC</span></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Initial State Registration</strong><br><span style="font-size:12px;color:var(--gray-500)">First-time application to register with one or more state securities authorities</span></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Annual Updating Amendment (SEC)</strong> — Fiscal year ended: <input type="date" style="display:inline;width:auto;padding:4px 8px;font-size:12px;margin-left:6px;"></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Other-Than-Annual Amendment</strong><br><span style="font-size:12px;color:var(--gray-500)">Promptly reporting a material change during the year</span></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Initial ERA Report to SEC</strong><br><span style="font-size:12px;color:var(--gray-500)">Exempt Reporting Adviser initial submission</span></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>ERA Report to State Authority</strong></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Annual ERA Amendment</strong> — Fiscal year ended: <input type="date" style="display:inline;width:auto;padding:4px 8px;font-size:12px;margin-left:6px;"></div></label>
    <label class="opt-item"><input type="checkbox" onchange="toggleClass(this,'opt-item','sel')"> <div><strong>Final Report</strong><br><span style="font-size:12px;color:var(--gray-500)">Withdrawing registration or ceasing ERA status</span></div></label>
  </div>
`,'filing-setup')}
${sub('Note','Important Reminders',`
  ${alert_('warn','⚠️','False statements carry serious consequences','Complete this form truthfully. False statements or omissions may result in denial of your application, revocation of your registration, or criminal prosecution. Keep this form updated by filing periodic amendments.')}
  ${alert_('info','📅','Annual filing deadline','Registered investment advisers must file their annual updating amendment within <strong>90 days</strong> after the end of their fiscal year.')}
`,'filing-note')}`
},

// ─────────────── SECTION 1: IDENTIFYING INFO ───────────────
{ id:'item1', short:'Item 1 — Identifying Info', item:'Item 1', title:'Identifying Information',
  subtitle:'Basic information about your firm — legal name, file numbers, address, and key contacts.',
  icon:'🏢',
  html:`
${sub('1A–1C','Names & Registration Numbers',`
  <div class="fg">
    <div class="gc-full">${field('Your full legal name','1A',inp('text','e.g. Pinnacle Capital Advisors LLC'),'If you are a sole proprietor, provide your last, first, and middle names.',true,'The exact legal name as it appears in your organizational documents or state registration.')}</div>
    ${field('Primary business name (if different from 1A)','1B(1)',inp('text','DBA name or trade name'),'Use this if you primarily conduct advisory business under a different name.',false,'List additional business names in Schedule D Section 1.B.',true)}
    ${field('Are you using this Form ADV for an umbrella registration?','',yn('umbrella-reg'),'If yes, complete a Schedule R for each relying adviser.',false,'An umbrella registration allows multiple related advisers to register jointly.')}
  </div>
  <hr class="divider">
  <div class="fg fg-2">
    ${field('SEC File Number','1D(1)',inp('text','801-XXXXX  or  802-XXXXX'),'Leave blank for an initial application. 801- for registered advisers; 802- for ERAs.',false,'Your existing file number if already registered or reporting to the SEC.',true)}
    ${field('Additional CIK Number(s)','1D(3)',inp('text','CIK number(s) if assigned by SEC'),'Central Index Key numbers assigned by the SEC.',false,'',true)}
    ${field('CRD Number (IARD/FINRA)','1E(1)',inp('text','e.g. 123456'),'Your FINRA CRD system or IARD system number.',false,'If your firm does not have a CRD number, skip this field. Do not provide an officer\'s or employee\'s CRD number.',true)}
    ${field('Additional CRD Number(s)','1E(2)',inp('text','Separate multiple with commas'),'','',false,true)}
    ${field('Legal Entity Identifier (LEI)','1P',inp('text','20-character alphanumeric LEI'),'A unique 20-character identifier used in financial markets.',false,'You may not have an LEI. Visit gleif.org to obtain one if needed.',true)}
    ${field('Name change — new name (if reporting a change)','1C',inp('text','New legal or primary business name'),'Only complete if this filing reports a change to your legal name (1A) or primary business name (1B).',false,'Specify in the hint below whether this is a legal name change or primary business name change.',true)}
  </div>
`,'1abc')}

${sub('1F','Principal Office & Place of Business',`
  ${alert_('warn','🚫','No P.O. Boxes','Your principal office must be a physical street address. P.O. Boxes are not acceptable.')}
  <div class="fg">
    <div class="gc-full">${field('Street address','1F(1)',inp('text','Number and street'),'',true)}</div>
  </div>
  <div class="fg fg-2">
    ${field('City','',inp('text','City'),'',true)}
    ${field('State / Country','',sel(STATES.concat(['Non-US (specify below)'])),'',true)}
    ${field('ZIP +4 / Postal code','',inp('text','00000-0000'),'',true)}
    ${field('If Non-US, specify country','',inp('text','Country name'),'','',false,true)}
    ${field('Is this a private residence?','',yn('principal-private'))}
    ${field('Normal business days','1F(2)',sel(['Monday – Friday','Monday – Saturday','Other']))}
    ${field('Normal business hours','1F(2)',inp('text','e.g. 8:00 AM – 5:00 PM EST'))}
    ${field('Telephone number','1F(3)',inp('tel','(000) 000-0000'),'',true)}
    ${field('Facsimile number','1F(4)',inp('tel','(000) 000-0000'),'','','',true)}
    ${field('Number of OTHER offices (not principal) where you conduct advisory business','1F(5)',inp('number','0'),'Count all other locations as of end of most recently completed fiscal year.')}
  </div>
`,'1f')}

${sub('1G–1H','Mailing Address & Sole Proprietor Residence',`
  <div class="fg fg-2">
    <div class="gc-full">${field('Mailing address (if different from principal office)','1G',inp('text','Street address'),'Leave blank if same as principal office.',false,'',true)}</div>
    ${field('City','',inp('text',''),'','','',true)} ${field('State/Country','',sel(STATES),'','','',true)}
    ${field('ZIP/Postal code','',inp('text',''),'','','',true)}
    ${field('Is mailing address a private residence?','',yn('mail-private'),'','','',true)}
  </div>
  <hr class="divider">
  <div class="alert alert-info"><div class="alert-icon">👤</div><div class="alert-body"><strong>Sole Proprietors Only</strong>If your residence differs from your principal office, provide it below.</div></div>
  <div class="fg fg-2">
    <div class="gc-full">${field('Sole proprietor residence address','1H',inp('text','Street address'),'','','',true)}</div>
    ${field('City','',inp('text',''),'','','',true)} ${field('State','',sel(STATES),'','','',true)}
    ${field('ZIP','',inp('text',''),'','','',true)}
  </div>
`,'1gh')}

${sub('1I','Websites & Social Media',`
  <div class="fg">
    ${field('Do you have websites or social media accounts?','1I',yn('has-website'),'If yes, list all firm accounts below.',true,'Do not list individual employee social media accounts or websites where you do not control the content.')}
  </div>
  <div id="websites-list" style="margin-top:12px;"></div>
  <button class="btn-add-entry" onclick="addWebsite()">+ Add Website or Social Media Account</button>
`,'1i')}

${sub('1J','Chief Compliance Officer',`
  ${alert_('info','👮','CCO Required','If you are registered or applying for registration with the SEC, you must designate a Chief Compliance Officer. There can only be one CCO.')}
  <div class="fg fg-2">
    ${field('CCO full legal name','1J(1)',inp('text','Last, First, Middle'),'',true)}
    ${field('Other titles or positions','',inp('text','e.g. General Counsel, COO'),'','','',true)}
    ${field('Telephone','',inp('tel','(000) 000-0000'),'',true)}
    ${field('Facsimile','',inp('tel','(000) 000-0000'),'','','',true)}
    ${field('Email address','',inp('email','cco@firm.com'),'',true)}
    <div class="gc-full">${field('CCO street address','',inp('text','Street address'))}</div>
    ${field('City','',inp('text',''))} ${field('State','',sel(STATES))}
    ${field('ZIP','',inp('text',''))}
    ${field('Is your CCO compensated or employed by a person other than you, a related person, or a registered investment company you advise?','1J(2)',yn('cco-outside'),'If yes, provide that person\'s details below.',false,'This applies when a third-party compliance firm provides CCO services.')}
  </div>
  <div class="conditional" id="cond-cco-outside">
    <div class="cond-indent">
      <div class="fg fg-2">
        ${field('Outside employer / firm name','1J(2)',inp('text','Name of third-party CCO firm or employer'),'',true)}
        ${field('Outside employer IRS EIN','',inp('text','XX-XXXXXXX'),'',true)}
      </div>
    </div>
  </div>
`,'1j')}

${sub('1K','Additional Regulatory Contact',`
  ${alert_('info','ℹ️','Optional','Only complete if a person other than the CCO is authorized to receive regulatory information and respond to questions about this Form ADV.')}
  <div class="fg fg-2">
    ${field('Contact name','',inp('text','Last, First, Middle'),'','','',true)}
    ${field('Titles','',inp('text','e.g. Director of Compliance'),'','','',true)}
    ${field('Telephone','',inp('tel','(000) 000-0000'),'','','',true)}
    ${field('Facsimile','',inp('tel','(000) 000-0000'),'','','',true)}
    ${field('Email','',inp('email',''),'','','',true)}
    <div class="gc-full">${field('Address','',inp('text','Street address'),'','','',true)}</div>
    ${field('City','',inp('text',''),'','','',true)} ${field('State','',sel(STATES),'','','',true)}
    ${field('ZIP','',inp('text',''),'','','',true)}
  </div>
`,'1k')}

${sub('1L–1O','Additional Required Disclosures',`
  <div class="fg">
    ${field('Do you maintain required books and records somewhere other than your principal office?','1L',yn('offsite-records'),'If yes, complete Section 1.L. of Schedule D in IARD.',false,'Required under Section 204 of the Advisers Act. The location must be accessible for inspection.')}
    ${field('Are you registered with a foreign financial regulatory authority?','1M',yn('foreign-reg'),'If yes, complete Section 1.M. of Schedule D.',false,'Answer "No" if only an affiliate is registered with a foreign authority — not your firm directly.')}
    ${field('Are you a public reporting company under Sections 12 or 15(d) of the Exchange Act of 1934?','1N',yn('public-reporting'),'Typical for advisers that are also publicly traded or have publicly registered securities.',false)}
    ${field('Did you have $1 billion or more in total firm assets on the last day of your most recent fiscal year?','1O',yn('billion-assets'),'"Total assets" here refers to your firm\'s total assets — not client assets under management.',false,'Use the total assets figure on your firm\'s balance sheet, not RAUM.')}
  </div>
  <div class="conditional" id="cond-billion-assets">
    <div class="cond-indent">
      ${field('Approximate amount of total assets:','1O',`<div class="opt-list inline">
        <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="asset-range"> $1B to less than $10B</label>
        <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="asset-range"> $10B to less than $50B</label>
        <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="asset-range"> $50B or more</label>
      </div>`,'',true)}
    </div>
  </div>
`,'1lo')}`
},

// ─────────────── SECTION 2: SEC REGISTRATION ───────────────
{ id:'item2', short:'Item 2 — SEC Registration', item:'Item 2', title:'SEC Registration Eligibility',
  subtitle:'Identify your basis for SEC registration or ERA status, and select states for notice filings.',
  icon:'🏛️',
  html:`
${sub('2A','Basis for SEC Registration',`
  ${alert_('info','📏','At least one required','You must check at least one box describing why you are eligible to register (or remain registered) with the SEC. If you are an ERA, skip to Item 2B.')}
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(1) Large Advisory Firm</strong> — RAUM of $100M or more <span class="rule-cite">Rule 203A-1(a)</span><br><span style="font-size:12px;color:var(--gray-500)">Also eligible if RAUM is $90M+ at time of most recent annual amendment and already registered with the SEC</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(2) Mid-Sized Advisory Firm</strong> — RAUM of $25M or more but less than $100M <span class="rule-cite">Rule 203A-1</span><br><span style="font-size:12px;color:var(--gray-500)">AND you are either (a) not required to be registered with the state where you have your principal office, OR (b) not subject to examination by that state</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')" style="opacity:0.4;pointer-events:none;"><input type="checkbox" disabled> <div><strong>(3) Reserved</strong></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(4) Non-U.S. Adviser</strong> — Principal office and place of business outside the United States</div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(5) Investment Company Adviser</strong> — Adviser or subadviser to an investment company registered under the Investment Company Act of 1940</div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(6) BDC Adviser</strong> — Adviser to a Business Development Company under §54 of the ICA with at least $25M RAUM</div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(7) Pension Consultant</strong> — Advise pension plans with aggregate assets ≥ $200M <span class="rule-cite">Rule 203A-2(a)</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(8) Related Adviser</strong> — Controls, is controlled by, or is under common control with an SEC-registered adviser; same principal office <span class="rule-cite">Rule 203A-2(b)</span><br><span style="font-size:12px;color:var(--gray-500)">Complete Section 2.A.(8) of Schedule D</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(9) Expects Eligibility Within 120 Days</strong> — Newly formed adviser <span class="rule-cite">Rule 203A-2(c)</span><br><span style="font-size:12px;color:var(--gray-500)">Complete Section 2.A.(9) of Schedule D. Must file amendment within 120 days of effectiveness.</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(10) Multi-State Adviser</strong> — Required to register in 15 or more states <span class="rule-cite">Rule 203A-2(d)</span><br><span style="font-size:12px;color:var(--gray-500)">Complete Section 2.A.(10) of Schedule D</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(11) Internet Adviser</strong> <span class="rule-cite">Rule 203A-2(e)</span><br><span style="font-size:12px;color:var(--gray-500)">Complete Section 2.A.(11) of Schedule D</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(12) SEC Exemption Order</strong> — SEC order exempting you from the prohibition against registration<br><span style="font-size:12px;color:var(--gray-500)">Complete Section 2.A.(12) of Schedule D</span></div></label>
    <label class="opt-item opt-item sel-warn" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(13) No Longer Eligible</strong> — No longer eligible to remain registered with the SEC<br><span style="font-size:12px;color:var(--gray-500)">⚠️ Check this when filing your annual amendment if your RAUM has fallen below $90M</span></div></label>
  </div>
`,'2a')}

${sub('2B','Exempt Reporting Adviser (ERA) Status',`
  ${alert_('info','📊','ERA Only','Complete only if you are reporting to the SEC as an exempt reporting adviser. Registered advisers should skip this section.')}
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(1) Venture Capital Fund Exemption</strong> <span class="rule-cite">Rule 203(l)-1</span><br><span style="font-size:12px;color:var(--gray-500)">Adviser solely to one or more venture capital funds as defined in Rule 203(l)-1</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(2) Private Fund Exemption (Under $150M)</strong> <span class="rule-cite">Rule 203(m)-1</span><br><span style="font-size:12px;color:var(--gray-500)">Adviser solely to private funds with U.S. AUM less than $150M. Complete Section 2.B. of Schedule D.</span></div></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> <div><strong>(3) Previously Checked (2) — Now $150M or More</strong><br><span style="font-size:12px;color:var(--gray-500)">No longer eligible for box 2 because U.S. AUM reached $150M. Complete Section 2.B. of Schedule D.</span></div></label>
  </div>
`,'2b')}

${sub('2C','State Notice Filings',`
  ${alert_('info','🗺️','Select applicable states','SEC-registered advisers may be required to provide notice filings to state securities authorities. ERAs may be required to provide reports. Select all states that should receive copies of this and all subsequent filings.')}
  ${stateGrid('notice-states')}
`,'2c')}`
},

// ─────────────── SECTION 3: ORGANIZATION ───────────────
{ id:'item3', short:'Item 3–4 — Organization', item:'Items 3–4', title:'Form of Organization & Successions',
  subtitle:'Your firm\'s legal structure, fiscal year, state of organization, and any business succession.',
  icon:'🏗️',
  html:`
${sub('3A–3C','Form of Organization',`
  ${alert_('warn','🔄','Name/structure changes','If you are changing your response to any Item 3 question due to a change in structure or legal status, see Part 1A Instruction 4 (Succession).')}
  <div class="fg fg-2">
    <div class="gc-full">${field('How are you organized?','3A',`<div class="opt-list inline">
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="corp"> Corporation</label>
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="sp"> Sole Proprietorship</label>
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="llc"> LLC</label>
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="lp"> LP</label>
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="llp"> LLP</label>
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="partner"> Partnership</label>
      <label class="opt-item" onclick="selOpt(this)"><input type="radio" name="org-type" value="other"> Other</label>
    </div>`,'',true,'Your form of organization determines how Schedules A and B should be completed.')}
    </div>
    ${field('If "Other," specify','',inp('text','Describe your form of organization'),'','','',true)}
    ${field('Month your fiscal year ends','3B',sel(['January','February','March','April','May','June','July','August','September','October','November','December'],'Month'),'Your annual amendment is due 90 days after this month ends.',true,'Your fiscal year end determines your annual filing deadline.')}
    ${field('State or country under whose laws you are organized','3C',inp('text','e.g. Delaware, New York, Cayman Islands'),'For partnerships: state of formation. For sole proprietors: state of residence.',true,'Most U.S. advisers are organized in Delaware, even if they operate elsewhere.')}
  </div>
`,'3abc')}

${sub('4','Successions',`
  <div class="fg">
    ${field('Are you succeeding to the business of a registered investment adviser at the time of this filing?','4A',yn('succession'),'Examples include: change in structure or legal status, merger, or acquisition of substantially all assets of a registered adviser.',false,'If yes, complete Item 4.B. and Section 4 of Schedule D. Do not re-report a succession you already reported on a previous filing.')}
  </div>
  <div class="conditional" id="cond-succession">
    <div class="cond-indent">
      ${field('Date of succession','4B',inp('date',''),'',true,'Enter the date the succession occurred, not the date of filing.')}
    </div>
  </div>
`,'4')}`
},

// ─────────────── SECTION 4: EMPLOYEES & CLIENTS ───────────────
{ id:'item5a', short:'Item 5A–D — Employees & Clients', item:'Item 5 (Employees & Clients)', title:'Employees & Client Information',
  subtitle:'Staff headcount, advisory functions, and a breakdown of your client base with associated regulatory assets under management.',
  icon:'👥',
  html:`
${sub('5A','Total Employees',`
  ${alert_('info','ℹ️','Who to count','Include all full-time and part-time employees. Do not include clerical, administrative, support, or similar workers. Sole proprietors: include yourself.')}
  ${field('Approximately how many employees does your firm have?','5A',inp('number','0'),'This is your firm\'s total headcount excluding clerical staff.',true)}
`,'5a')}

${sub('5B','Employee Breakdown',`
  ${alert_('info','ℹ️','Double-counting OK here','If an employee performs more than one function, count them in each applicable row below.')}
  <div class="fg fg-2">
    ${field('(1) Employees performing investment advisory functions (including research)','5B(1)',inp('number','0'),'',true,'Includes portfolio managers, analysts, and anyone who provides investment advice.')}
    ${field('(2) Registered representatives of a broker-dealer','5B(2)',inp('number','0'),'',true)}
    ${field('(3) Registered as investment adviser representatives with one or more state securities authorities FOR YOUR FIRM','5B(3)',inp('number','0'),'',true)}
    ${field('(4) Registered as investment adviser representatives FOR ANOTHER investment adviser (not your firm)','5B(4)',inp('number','0'),'',true,'These are dual-registrants affiliated with another advisory firm.')}
    ${field('(5) Licensed as agents of an insurance company or agency','5B(5)',inp('number','0'),'',true)}
    ${field('(6) Firms or persons who solicit advisory clients on your behalf (count each firm once, not its individual employees)','5B(6)',inp('number','0'),'',true,'Third-party solicitors/promoters. Do not include your own employees.')}
  </div>
`,'5b')}

${sub('5C','Non-RAUM Clients',`
  <div class="fg fg-2">
    ${field('Number of clients for whom you do NOT have regulatory assets under management (e.g., financial planning only)','5C(1)',inp('number','0'),'Do not include investors in a private fund you advise unless you have a separate advisory relationship with them.',true,'This covers clients who receive financial planning, consulting, or other advice without you managing their portfolio.')}
    ${field('Approximate percentage of all your clients who are non-United States persons','5C(2)',addon(inp('number','0','min=0 max=100 step=1'),'%'),'',true)}
  </div>
`,'5c')}

${sub('5D','Client & RAUM Table by Client Type',`
  ${alert_('info','📊','Completion requirement','Provide (1) number of clients OR check "Fewer than 5" AND (3) the RAUM amount for each type. The total RAUM column must equal your answer to Item 5F(2)(c). If a client fits multiple categories, choose the most accurate one.')}
  <div class="sched-table-wrap">
  <table class="sched-table">
    <thead><tr>
      <th style="width:42%">Type of Client</th>
      <th style="width:16%">Number of Clients (1)</th>
      <th style="width:12%;text-align:center">Fewer Than 5? (2)</th>
      <th style="width:22%">RAUM Amount ($) (3)</th>
    </tr></thead>
    <tbody>
      ${[['(a) Individuals (other than high net worth)'],['(b) High net worth individuals'],['(c) Banking or thrift institutions'],['(d) Investment companies (registered under ICA 1940)'],['(e) Business development companies'],['(f) Pooled investment vehicles (other than investment companies and BDCs)'],['(g) Pension and profit sharing plans (not plan participants or government plans)'],['(h) Charitable organizations'],['(i) State or municipal government entities (including government pension plans)'],['(j) Other investment advisers'],['(k) Insurance companies'],['(l) Sovereign wealth funds and foreign official institutions'],['(m) Corporations or other businesses not listed above'],['(n) Other (specify below)']].map(([l])=>`<tr>
        <td>${l}</td>
        <td><input type="number" min="0" placeholder="0"></td>
        <td style="text-align:center"><input type="checkbox" style="width:auto;accent-color:var(--navy);width:16px;height:16px;"></td>
        <td><input type="number" min="0" placeholder="$0" step="1000"></td>
      </tr>`).join('')}
    </tbody>
  </table>
  </div>
  <div style="margin-top:12px;">${field('If "Other" in row (n), describe the client type:','',inp('text',''),'','','',true)}</div>
`,'5d')}`
},

// ─────────────── SECTION 5: RAUM & ADVISORY SERVICES ───────────────
{ id:'item5b', short:'Item 5E–L — RAUM & Services', item:'Item 5 (RAUM & Services)', title:'RAUM, Services & Marketing',
  subtitle:'Your regulatory assets under management, types of advisory services, wrap fee programs, and marketing practices.',
  icon:'📈',
  html:`
${sub('5E','Compensation Arrangements',`
  ${alert_('info','ℹ️','Check all that apply','Select every method by which your firm is compensated for investment advisory services.')}
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (1) A percentage of assets under your management (AUM fee)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (2) Hourly charges</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (3) Subscription fees (for a newsletter or periodical)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (4) Fixed fees (other than subscription fees)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (5) Commissions</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (6) Performance-based fees <span class="tag-pill tag-new">Note: triggers additional disclosures in Part 2A</span></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (7) Other (specify below)</label>
  </div>
  ${field('If "Other" (7) — describe:','',inp('text',''),'','','',true)}
`,'5e')}

${sub('5F','Regulatory Assets Under Management (RAUM)',`
  ${alert_('info','💡','How to calculate RAUM','Follow Part 1A Instruction 5.b. carefully. RAUM includes all securities portfolios for which you provide continuous and regular supervisory or management services — including family accounts. It does not include assets you manage on a non-continuous basis.')}
  <div class="fg">
    ${field('Do you provide continuous and regular supervisory or management services to securities portfolios?','5F(1)',yn('supervisory-services'),'If yes, complete the RAUM table below.',true)}
  </div>
  <div class="conditional show" id="cond-supervisory-services">
    <div style="margin-top:16px;">
    <div class="sched-table-wrap">
    <table class="sched-table">
      <thead><tr><th></th><th>U.S. Dollar Amount (RAUM)</th><th>Total Number of Accounts</th></tr></thead>
      <tbody>
        <tr><td><strong>Discretionary</strong> <span class="field-ref">5F(2)(a)/(d)</span></td><td>${addon(inp('number','0','step=1000 min=0'),'USD')}</td><td><input type="number" placeholder="0" min="0"></td></tr>
        <tr><td><strong>Non-Discretionary</strong> <span class="field-ref">5F(2)(b)/(e)</span></td><td>${addon(inp('number','0','step=1000 min=0'),'USD')}</td><td><input type="number" placeholder="0" min="0"></td></tr>
        <tr style="background:var(--blue-soft)"><td><strong>Total</strong> <span class="field-ref">5F(2)(c)/(f)</span></td><td>${addon(inp('number','0','step=1000 min=0 style="font-weight:600"'),'USD')}</td><td><input type="number" placeholder="0" min="0" style="font-weight:600;"></td></tr>
      </tbody>
    </table>
    </div>
    <div style="margin-top:14px;">${field('RAUM attributable to non-United States persons (approximate)','5F(3)',addon(inp('number','0','min=0 step=1000'),'USD'),'Subset of total RAUM in 5F(2)(c).')}</div>
    </div>
  </div>
`,'5f')}

${sub('5G','Types of Advisory Services',`
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (1) Financial planning services</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (2) Portfolio management for individuals and/or small businesses</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (3) Portfolio management for investment companies (including BDCs) — <em>only if you have an investment advisory contract with a registered investment company</em></label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (4) Portfolio management for pooled investment vehicles (other than investment companies)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (5) Portfolio management for businesses (other than small businesses) or institutional clients (other than registered investment companies)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (6) Pension consulting services</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (7) Selection of other advisers (including private fund managers)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (8) Publication of periodicals or newsletters</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (9) Security ratings or pricing services</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (10) Market timing services</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (11) Educational seminars/workshops</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (12) Other (specify below)</label>
  </div>
  <div style="margin-top:12px;" class="fg fg-2">
    ${field('If (3) checked — 811 or 814 number(s) of registered investment company/companies advised','Sched D 5G(3)',inp('text','e.g. 811-XXXXX'),'Required if you manage any registered investment companies.',false,'',true)}
    ${field('If (12) checked — describe other advisory services:','',inp('text',''),'','','',true)}
  </div>
  <div style="margin-top:16px;">
    ${field('To how many clients did you provide financial planning services during your last fiscal year?','5H',`<div class="opt-list inline">
      ${['0','1–10','11–25','26–50','51–100','101–250','251–500','More than 500'].map(v=>`<label class="opt-item" onclick="selOpt(this)"><input type="radio" name="fp-clients" value="${v}"> ${v}</label>`).join('')}
    </div>`,'Only applicable if you checked (1) above.')}
    ${field('If more than 500 — how many? (round to nearest 500)','5H',inp('number','500','min=500 step=500'),'','','',true)}
  </div>
`,'5gh')}

${sub('5I','Wrap Fee Programs',`
  <div class="fg">
    ${field('Do you participate in a wrap fee program?','5I(1)',yn('wrap-fee'),'A wrap fee program bundles advisory, brokerage, and other services for a single bundled fee.',false,'If yes, complete Schedule D Section 5.I.(2) listing program names and sponsors for each program where you are a portfolio manager.')}
  </div>
  <div class="conditional" id="cond-wrap-fee">
    <div class="cond-indent">
      <div class="fg fg-2">
        ${field('RAUM as <strong>sponsor</strong> to a wrap fee program','5I(2)(a)',addon(inp('number','0','min=0 step=1000'),'USD'))}
        ${field('RAUM as <strong>portfolio manager</strong> for a wrap fee program','5I(2)(b)',addon(inp('number','0','min=0 step=1000'),'USD'))}
        <div class="gc-full">${field('RAUM as <strong>both</strong> sponsor AND portfolio manager for the <em>same</em> program (do NOT also report in (a) or (b))','5I(2)(c)',addon(inp('number','0','min=0 step=1000'),'USD'))}</div>
      </div>
    </div>
  </div>
`,'5i')}

${sub('5J–5K','Part 2A Consistency & SMA Clients',`
  <div class="fg">
    ${field('In your Part 2A (Item 4.B.), do you indicate that you provide investment advice only with respect to limited types of investments?','5J(1)',yn('limited-inv-types'),'A "Yes" means your brochure discloses investment type restrictions.',false,'Common for advisers who only provide advice on equities, bonds, or alternatives.')}
    ${field('Do you report client assets in Part 2A Item 4.E. using a different method than the method used to compute RAUM in Item 5F?','5J(2)',yn('diff-method'),'If yes, you should explain the methodology difference in Part 2A.',false)}
    ${field('Do you have RAUM attributable to separately managed account (SMA) clients (i.e., clients other than those in 5D(d)–(f))?','5K(1)',yn('sma-clients'),'If yes, complete Section 5.K.(1) of Schedule D.',false,'SMA clients are typically high-net-worth individuals or institutions with separately managed portfolios.')}
    ${field('Do you engage in <strong>borrowing transactions</strong> on behalf of any SMA clients?','5K(2)',yn('sma-borrowing'),'If yes, complete Section 5.K.(2) of Schedule D.',false)}
    ${field('Do you engage in <strong>derivative transactions</strong> on behalf of any SMA clients?','5K(3)',yn('sma-derivatives'),'If yes, complete Section 5.K.(2) of Schedule D.',false)}
    ${field('After subtracting RAUM in 5D(d)–(f), does any single custodian hold <strong>10% or more</strong> of your remaining RAUM?','5K(4)',yn('custodian-10pct'),'If yes, complete Section 5.K.(3) of Schedule D for each such custodian.',false,'This concentration disclosure helps the SEC monitor custodial risk.')}
  </div>
`,'5jk')}

${sub('5L','Marketing Activities',`
  ${alert_('purple','📣','Marketing Rule','These questions reflect the SEC\'s Investment Adviser Marketing Rule (Rule 206(4)-1), effective May 4, 2021. "Advertisements" under the rule includes client communications, website content, and third-party promotions.')}
  <div style="margin-bottom:12px;"><strong style="font-size:13px;color:var(--gray-700)">5L(1) — Do any of your advertisements include:</strong></div>
  <div class="fg">
    ${field('(a) Performance results?','5L(1)(a)',yn('mktg-perf'),'Includes actual performance and backtested performance.',false,'If yes, ensure your advertisements comply with Rule 206(4)-1 requirements for performance presentations.')}
    ${field('(b) A reference to specific investment advice provided by you? <span class="rule-cite">Rule 206(4)-1(a)(5)</span>','5L(1)(b)',yn('mktg-specific-advice'),'Includes case studies or specific investment recommendations.',false)}
    ${field('(c) Testimonials (other than those satisfying Rule 206(4)-1(b)(4)(ii))?','5L(1)(c)',yn('mktg-testimonials'),'Client statements about your services. Certain testimonials require disclosures.',false,'Testimonials from clients must comply with the rule\'s disclosure requirements unless they qualify for the de minimis exception.')}
    ${field('(d) Endorsements (other than those satisfying Rule 206(4)-1(b)(4)(ii))?','5L(1)(d)',yn('mktg-endorsements'),'Statements from non-clients (e.g., celebrities, industry professionals).',false)}
    ${field('(e) Third-party ratings?','5L(1)(e)',yn('mktg-ratings'),'Rankings or ratings from third parties such as Barron\'s, Forbes, or Morningstar.',false)}
    ${field('5L(2) — If yes to (c), (d), or (e): Do you pay or provide cash or non-cash compensation in connection with those testimonials, endorsements, or ratings?','5L(2)',yn('mktg-compensation'),'Triggers solicitor/promoter disclosure and written agreement requirements.',false,'Even non-cash compensation (gifts, discounts, fee waivers) counts here.')}
    ${field('5L(3) — Do any advertisements include <strong>hypothetical performance</strong>?','5L(3)',yn('mktg-hypothetical'),'Includes model performance, backtested results, or projected returns.',false,'Hypothetical performance has strict compliance requirements under the Marketing Rule.')}
    ${field('5L(4) — Do any advertisements include <strong>predecessor performance</strong>?','5L(4)',yn('mktg-predecessor'),'Performance from a prior firm or strategy you or key personnel managed.',false)}
  </div>
`,'5l')}`
},

// ─────────────── SECTION 6: OTHER BUSINESS ───────────────
{ id:'item6', short:'Item 6 — Other Business', item:'Item 6', title:'Other Business Activities',
  subtitle:'Business activities outside of investment advice, and whether you sell other products or services to your advisory clients.',
  icon:'💼',
  html:`
${sub('6A','Active Business Engagements',`
  ${alert_('info','ℹ️','Check all that apply','These are the other businesses in which you are currently active. If you conduct any of these under a different name from Items 1A or 1B, complete Section 6.A. of Schedule D.')}
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (1) Broker-dealer (registered or unregistered)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (2) Registered representative of a broker-dealer</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (3) Commodity pool operator (CPO) or commodity trading adviser (CTA) — registered or exempt</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (4) Futures commission merchant</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (5) Real estate broker, dealer, or agent</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (6) Insurance broker or agent</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (7) Bank (including a separately identifiable department or division of a bank)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (8) Trust company</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (9) Registered municipal advisor</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (10) Registered security-based swap dealer</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (11) Major security-based swap participant</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (12) Accountant or accounting firm</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (13) Lawyer or law firm</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (14) Other financial product salesperson (specify below)</label>
  </div>
  ${field('If (14) checked — specify other financial product sales activity:','',inp('text',''),'','','',true)}
`,'6a')}

${sub('6B','Other Non-Advisory Business',`
  <div class="fg">
    ${field('Are you actively engaged in any other business NOT listed in Item 6A (other than giving investment advice)?','6B(1)',yn('other-biz'),'',false,'Examples: consulting, speaking engagements, or other professional services unrelated to the above.')}
  </div>
  <div class="conditional" id="cond-other-biz">
    <div class="cond-indent">
      <div class="fg">
        ${field('Is this other business your primary business?','6B(2)',yn('other-biz-primary'),'If the non-advisory activity takes more of your time than your advisory business.',true)}
        ${field('Describe the other business (and approximate time spent):','6B(2)',`<textarea placeholder="Describe the nature of the business activity and approximately what percentage of your time it represents…"></textarea>`,'Required — also complete Section 6.B.(2) of Schedule D in IARD.',true)}
        ${field('Name under which you conduct the other business (if different from Items 1A/1B):','',inp('text',''),'','','',true)}
      </div>
    </div>
  </div>
  <hr class="divider">
  <div class="fg">
    ${field('Do you sell products or provide services other than investment advice to your advisory clients?','6B(3)',yn('sell-other-products'),'Examples: insurance products, tax preparation, estate planning, or real estate.',false,'This is a key conflict-of-interest disclosure. If yes, complete Section 6.B.(3) of Schedule D and describe in Part 2A.')}
  </div>
  <div class="conditional" id="cond-sell-other-products">
    <div class="cond-indent">
      ${field('Describe the products/services sold to advisory clients:','6B(3)',`<textarea placeholder="Describe the products or services and any compensation you receive for them…"></textarea>`,'Also complete Section 6.B.(3) of Schedule D.',true)}
      ${field('Business name (if different from Items 1A/1B):','',inp('text',''),'','','',true)}
    </div>
  </div>
`,'6b')}`
},

// ─────────────── SECTION 7: AFFILIATIONS & PRIVATE FUNDS ───────────────
{ id:'item7', short:'Item 7 — Affiliations & Private Funds', item:'Item 7', title:'Financial Industry Affiliations & Private Funds',
  subtitle:'Related person affiliations and details about any private funds you advise.',
  icon:'🔗',
  html:`
${sub('7A','Related Person Affiliations',`
  ${alert_('info','🔗','What is a related person?','"Related persons" include all your advisory affiliates and any person under common control with you — including foreign affiliates. For each checked category below, complete Section 7.A. of Schedule D (unless all five exemption conditions in the instructions are met).')}
  ${alert_('warn','📝','Schedule D required','You must complete a Schedule D Section 7.A. entry for each related person you identify below, including any that act as qualified custodians for your clients.')}
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (1) Broker-dealer, municipal securities dealer, or government securities broker or dealer (registered or unregistered)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (2) Other investment adviser (including financial planners)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (3) Registered municipal advisor</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (4) Registered security-based swap dealer</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (5) Major security-based swap participant</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (6) Commodity pool operator (CPO) or commodity trading adviser (CTA)</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (7) Futures commission merchant</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (8) Banking or thrift institution</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (9) Trust company</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (10) Accountant or accounting firm</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (11) Lawyer or law firm</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (12) Insurance company or agency</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (13) Pension consultant</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (14) Real estate broker or dealer</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (15) Sponsor or syndicator of limited partnerships (or equivalent), excluding pooled investment vehicles</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (16) Sponsor, general partner, managing member (or equivalent) of pooled investment vehicles</label>
  </div>
`,'7a')}

${sub('7B','Private Fund Adviser Disclosure',`
  <div class="fg">
    ${field('Are you an adviser to any private fund?','7B',yn('private-fund-adviser'),'A private fund includes any hedge fund, private equity fund, venture capital fund, real estate fund, or other pooled investment vehicle that relies on Section 3(c)(1) or 3(c)(7) of the ICA.',true,'If yes, complete Section 7.B.(1) of Schedule D for each fund you are the primary adviser for. If a co-adviser already reported the fund, complete Section 7.B.(2) instead.')}
  </div>
  <div class="conditional" id="cond-private-fund-adviser">
    <div id="pf-list" style="margin-top:12px;"></div>
    <button class="btn-add-entry" onclick="addPrivateFund()">+ Add Private Fund</button>
  </div>
`,'7b')}`
},

// ─────────────── SECTION 8: CLIENT TRANSACTIONS ───────────────
{ id:'item8', short:'Item 8 — Client Transactions', item:'Item 8', title:'Participation or Interest in Client Transactions',
  subtitle:'Disclose how you and your related persons participate in — or have interests in — your clients\' transactions.',
  icon:'⚖️',
  html:`
  ${alert_('warn','⚠️','Answer for yourself AND all related persons','Respond "Yes" if you OR any related person (including foreign affiliates) engages in the activity. Newly-formed advisers: base responses on activities you expect to engage in during the next year.')}

${sub('8A','Proprietary Interest in Client Transactions',`
  ${discRow('(1) Do you or any related person <strong>buy securities for yourself from advisory clients, or sell securities you own to advisory clients</strong> (<em>principal transactions</em>)?','8a1','Regulatory Action')}
  ${discRow('(2) Do you or any related person <strong>buy or sell for yourself securities</strong> (other than mutual fund shares) <strong>that you also recommend to advisory clients</strong>?','8a2',null)}
  ${discRow('(3) Do you or any related person <strong>recommend securities to advisory clients in which you or any related person has a proprietary (ownership) interest</strong> other than those in (1) or (2)?','8a3',null)}
`,'8a')}

${sub('8B','Sales Interest in Client Transactions',`
  ${discRow('(1) As a broker-dealer or registered representative, do you or any related person <strong>execute securities trades for brokerage customers in which advisory client securities are sold to or bought from the brokerage customer</strong> (<em>agency cross transactions</em>)?','8b1',null)}
  ${discRow('(2) Do you or any related person <strong>recommend securities to advisory clients for which you or a related person serves as underwriter or general/managing partner</strong>?','8b2',null)}
  ${discRow('(3) Do you or any related person have any <strong>other sales interest</strong> in securities recommended to advisory clients (other than receipt of sales commissions as a broker)?','8b3',null)}
`,'8b')}

${sub('8C–F','Brokerage Discretion & Broker Relationships',`
  ${discRow('(C1) Do you or any related person have <strong>discretionary authority to determine the securities</strong> to be bought or sold for a client\'s account?','8c1',null)}
  ${discRow('(C2) Do you or any related person have <strong>discretionary authority to determine the amount</strong> of securities to be bought or sold for a client\'s account?','8c2',null)}
  ${discRow('(C3) Do you or any related person have <strong>discretionary authority to determine the broker or dealer</strong> to be used for client securities transactions?','8c3',null)}
  ${discRow('(C4) Do you or any related person have <strong>discretionary authority to determine the commission rates</strong> to be paid to a broker or dealer?','8c4',null)}
  ${discRow('(D) If yes to C(3) — are any of those brokers or dealers <strong>related persons</strong>?','8d',null)}
  ${discRow('(E) Do you or any related person <strong>recommend brokers or dealers</strong> to clients?','8e',null)}
  ${discRow('(F) If yes to E — are any of those recommended brokers or dealers <strong>related persons</strong>?','8f',null)}
`,'8cf')}

${sub('8G–I','Soft Dollars & Client Referrals',`
  ${alert_('info','💵','Soft dollar safe harbor','Section 28(e) of the Exchange Act provides a safe harbor for certain "research or brokerage services" received in connection with client transactions. Not all soft dollar benefits qualify.')}
  ${discRow('(G1) Do you or any related person receive <strong>research or other products or services other than execution</strong> from a broker-dealer or third party ("<em>soft dollar benefits</em>") in connection with client securities transactions?','8g1',null)}
  ${discRow('(G2) If yes to G(1) — are <strong>ALL</strong> soft dollar benefits received eligible "research or brokerage services" under Section 28(e) of the Exchange Act?','8g2',null)}
  <hr class="divider">
  ${alert_('info','👥','Referral compensation','For Items 8H and 8I, consider all cash and non-cash compensation given or received for client referrals, including any bonus based at least in part on referral volume.')}
  ${discRow('(H1) Do you or any related person, directly or indirectly, <strong>compensate any non-employee person for client referrals</strong>?','8h1',null)}
  ${discRow('(H2) Do you or any related person provide any <strong>employee compensation specifically related to obtaining clients</strong> (cash or non-cash, beyond regular salary)?','8h2',null)}
  ${discRow('(I) Do you or any related person (including employees) directly or indirectly <strong>receive compensation from any person other than you or a related person for client referrals</strong>? (Do not include regular employee salary.)','8i',null)}
`,'8gi')}`
},

// ─────────────── SECTION 9: CUSTODY ───────────────
{ id:'item9', short:'Item 9 — Custody', item:'Item 9', title:'Custody',
  subtitle:'Whether you or your related persons have custody of client assets, and what custodial safeguards are in place.',
  icon:'🔒',
  html:`
  ${alert_('warn','⚠️','Custody triggers enhanced obligations','If you have custody, you must comply with the Custody Rule (Rule 206(4)-2). This includes qualified custodian requirements, account statements, and potentially surprise examinations or audits.')}
  ${alert_('info','ℹ️','When to answer "No" for SEC registrants','If you are SEC-registered and you have custody solely because (i) you deduct advisory fees directly, or (ii) a related person has custody but you have overcome the operational independence presumption — answer "No" to 9A(1)(a) and (b).')}

${sub('9A','Your Custody of Client Assets',`
  <div class="fg">
    ${field('(1)(a) Do <strong>you</strong> have custody of any advisory clients\' <em>cash or bank accounts</em>?','9A(1)(a)',yn('9a1a'),'',true)}
    ${field('(1)(b) Do <strong>you</strong> have custody of any advisory clients\' <em>securities</em>?','9A(1)(b)',yn('9a1b'),'',true)}
  </div>
  <div class="conditional" id="cond-9a">
    <div class="cond-indent">
      <div class="fg fg-2">
        ${field('Approximate total amount of client funds & securities for which YOU have custody','9A(2)(a)',addon(inp('number','0','min=0 step=1000'),'USD'),'',true)}
        ${field('Total number of clients for which you have custody','9A(2)(b)',inp('number','0','min=0'),'',true)}
      </div>
    </div>
  </div>
`,'9a')}

${sub('9B','Related Person Custody',`
  ${alert_('info','ℹ️','Always answer this','Complete Items 9B(1)(a) and (b) regardless of how you answered 9A.')}
  <div class="fg">
    ${field('(1)(a) Do any <strong>related persons</strong> have custody of any advisory clients\' <em>cash or bank accounts</em>?','9B(1)(a)',yn('9b1a'),'',true)}
    ${field('(1)(b) Do any <strong>related persons</strong> have custody of any advisory clients\' <em>securities</em>?','9B(1)(b)',yn('9b1b'),'',true)}
  </div>
  <div class="conditional" id="cond-9b">
    <div class="cond-indent">
      <div class="fg fg-2">
        ${field('Approximate amount of client funds & securities for which RELATED PERSONS have custody','9B(2)(a)',addon(inp('number','0','min=0 step=1000'),'USD'),'',true)}
        ${field('Total number of clients for which related persons have custody','9B(2)(b)',inp('number','0','min=0'),'',true)}
      </div>
    </div>
  </div>
`,'9b')}

${sub('9C','Custodial Safeguards',`
  ${alert_('info','📋','Check all that apply','If you or your related persons have custody, at least one of these safeguards should apply.')}
  <div class="opt-list">
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (1) A qualified custodian sends account statements at <strong>least quarterly</strong> to investors in the pooled investment vehicles you manage</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (2) An independent public accountant <strong>annually audits</strong> the pooled investment vehicles you manage, and audited financial statements are distributed to investors</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (3) An independent public accountant conducts an <strong>annual surprise examination</strong> of client funds and securities</label>
    <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox"> (4) An independent public accountant prepares an <strong>internal control report</strong> for custodial services when you or your related persons act as qualified custodians</label>
  </div>
  ${alert_('info','📝','If checked (2), (3), or (4)','List the accountants in Section 9.C. of Schedule D. (Exception: auditor info for (2) not required if already provided in Schedule D 7.B.(1) for private funds.)')}
  <div id="auditors-list" style="margin-top:12px;"></div>
  <button class="btn-add-entry" onclick="addAuditor()">+ Add Accountant / Auditor</button>
`,'9c')}

${sub('9D–F','Qualified Custodians',`
  <div class="fg">
    ${field('Do you or your related persons act as <strong>qualified custodians</strong> for clients?','9D',`<div class="opt-list">
      <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox" name="qc-self"> (1) You act as a qualified custodian</label>
      <label class="opt-item" onclick="toggleClass(this,'opt-item','sel')"><input type="checkbox" name="qc-related"> (2) Related person(s) act as qualified custodian(s) — if checked, identify all such related persons in Schedule D Section 7.A.</label>
    </div>`,'',false,'Acting as a qualified custodian triggers the internal control report requirement (9C(4)).')}
    ${field('Date your surprise examination commenced (MM/YYYY)','9E',inp('text','MM/YYYY'),'Complete only if you are filing an annual updating amendment and were subject to a surprise examination during the last fiscal year.',false,'',true)}
    ${field('Total number of persons (including you and related persons) who act as qualified custodians for your clients','9F',inp('number','0'),'',false)}
  </div>
`,'9df')}`
},

// ─────────────── SECTION 10: CONTROL PERSONS ───────────────
{ id:'item10', short:'Item 10 — Control Persons', item:'Item 10', title:'Control Persons & Ownership',
  subtitle:'Identify everyone who directly or indirectly controls your management or policies, and complete Schedules A and B.',
  icon:'🏛️',
  html:`
  ${alert_('info','📖','What is "control"?','"Control" means the power to direct or cause the direction of the management or policies of a person, whether through ownership of securities, by contract, or otherwise. Any person with 25%+ voting rights or 25%+ of profits is <strong>presumed</strong> to have control.')}

${sub('10A–B','Control Person Questions',`
  <div class="fg">
    ${field('Does any person NOT named in Item 1.A. or Schedules A, B, or C directly or indirectly control your management or policies?','10A',yn('additional-control'),'If yes, complete Section 10.A. of Schedule D.',true,'Controlling persons may include a parent company, majority shareholder, or any person who can direct your advisory business through contract or other means.')}
    ${field('Is any person named in Schedules A, B, C, or Section 10.A. of Schedule D a <strong>public reporting company</strong> under Sections 12 or 15(d) of the Exchange Act?','10B',yn('public-reporting-control'),'If yes, complete Section 10.B. of Schedule D.',true)}
  </div>
`,'10ab')}

${sub('Sched A','Schedule A — Direct Owners & Executive Officers',`
  ${alert_('info','📋','Who to list on Schedule A','List: (a) CEO, CFO, COO, CLO, CCO, Directors, and persons with similar functions; (b) shareholders with direct ownership of 5%+ of any class of voting securities; (c) for partnerships: all general partners and 5%+ limited partners; (d) for trusts: the trust entity and each trustee; (e) for LLCs: 5%+ members and all elected managers.<br><br><strong>Ownership codes:</strong> NA=&lt;5% | A=5–&lt;10% | B=10–&lt;25% | C=25–&lt;50% | D=50–&lt;75% | E=75%+')}
  <div id="sched-a-list"></div>
  <button class="btn-add-entry" onclick="addSchedA()">+ Add Direct Owner / Executive Officer</button>
  <div style="margin-top:12px;">${field('Do you have indirect owners to report on Schedule B?','',yn('has-indirect-owners'),'',true)}</div>
`,'sched-a')}

${sub('Sched B','Schedule B — Indirect Owners',`
  ${alert_('info','📋','Who to list on Schedule B','For each entity on Schedule A, list 25%+ owners going up the ownership chain until you reach a public reporting company. Include: (a) for corporations: 25%+ shareholders; (b) for partnerships: all general partners and 25%+ limited partners; (c) for trusts: the trust and each trustee; (d) for LLCs: 25%+ members and all elected managers.')}
  <div id="sched-b-list"></div>
  <button class="btn-add-entry" onclick="addSchedB()">+ Add Indirect Owner</button>
`,'sched-b')}`
},

// ─────────────── SECTION 11: DISCLOSURES ───────────────
{ id:'item11', short:'Item 11 — Disclosure Information', item:'Item 11', title:'Disclosure Information',
  subtitle:'Criminal, regulatory, civil, and financial disciplinary history for you and all your advisory affiliates.',
  icon:'⚠️',
  html:`
  ${alert_('error','🚨','DRP required for every "Yes"','You must complete the appropriate Disclosure Reporting Page (DRP) in IARD for each "Yes" answer below. One event may result in "Yes" answers to multiple questions. Advisory affiliates include: (1) all current non-clerical employees; (2) all officers, partners, and directors; and (3) all persons controlling or controlled by you.')}
  ${alert_('info','⏱️','10-year lookback for SEC registrants','If registered or registering with the SEC, you may limit most disclosures to events occurring within the past 10 years.')}

${sub('11A–B','Criminal Disclosures',`
  <div class="alert alert-info"><div class="alert-icon">📄</div><div class="alert-body"><strong>Criminal Action DRP required for any "Yes"</strong>Complete a Criminal Action DRP in IARD for each event.</div></div>
  ${discRow('(A1) In the past 10 years, have you or any advisory affiliate been <strong>convicted of or pled guilty or no contest to any felony</strong>?','11a1','Criminal Action')}
  ${discRow('(A2) In the past 10 years, have you or any advisory affiliate been <strong>charged with any felony</strong>? (SEC registrants: may limit to currently pending charges)','11a2','Criminal Action')}
  <hr class="divider">
  ${discRow('(B1) In the past 10 years, have you or any advisory affiliate been <strong>convicted of or pled guilty or no contest to a misdemeanor</strong> involving: investments or an investment-related business, fraud, false statements or omissions, wrongful taking of property, bribery, perjury, forgery, counterfeiting, extortion, or conspiracy to commit any of these?','11b1','Criminal Action')}
  ${discRow('(B2) In the past 10 years, have you or any advisory affiliate been <strong>charged with a misdemeanor</strong> listed in 11B(1)? (SEC registrants: may limit to currently pending charges)','11b2','Criminal Action')}
`,'11ab')}

${sub('11C','SEC / CFTC Regulatory Actions',`
  <div class="alert alert-info"><div class="alert-icon">📄</div><div class="alert-body"><strong>Regulatory Action DRP required for any "Yes"</strong></div></div>
  ${discRow('(C1) Has the SEC or CFTC ever found you or any advisory affiliate to have <strong>made a false statement or omission</strong>?','11c1','Regulatory Action')}
  ${discRow('(C2) Has the SEC or CFTC ever found you or any advisory affiliate to have been involved in a <strong>violation of SEC or CFTC regulations or statutes</strong>?','11c2','Regulatory Action')}
  ${discRow('(C3) Has the SEC or CFTC ever found you or any advisory affiliate to have been a cause of an investment-related business having its authorization to do business <strong>denied, suspended, revoked, or restricted</strong>?','11c3','Regulatory Action')}
  ${discRow('(C4) Has the SEC or CFTC ever entered an <strong>order against you or any advisory affiliate</strong> in connection with investment-related activity?','11c4','Regulatory Action')}
  ${discRow('(C5) Has the SEC or CFTC ever imposed a <strong>civil money penalty</strong>, or ordered you or any advisory affiliate to <strong>cease and desist</strong> from any activity?','11c5','Regulatory Action')}
`,'11c')}

${sub('11D','Other Federal, State & Foreign Regulatory Actions',`
  <div class="alert alert-info"><div class="alert-icon">📄</div><div class="alert-body"><strong>Regulatory Action DRP required for any "Yes"</strong></div></div>
  ${discRow('(D1) Has any other federal regulatory agency, state regulatory agency, or foreign financial regulatory authority ever found you or any advisory affiliate to have <strong>made a false statement or omission, or been dishonest, unfair, or unethical</strong>?','11d1','Regulatory Action')}
  ${discRow('(D2) Has any such agency ever found you or any advisory affiliate to have been involved in a <strong>violation of investment-related regulations or statutes</strong>?','11d2','Regulatory Action')}
  ${discRow('(D3) Has any such agency ever found you or any advisory affiliate to have been a cause of an investment-related business having its authorization to do business <strong>denied, suspended, revoked, or restricted</strong>?','11d3','Regulatory Action')}
  ${discRow('(D4) In the past 10 years, has any such agency entered an <strong>order against you or any advisory affiliate</strong> in connection with an investment-related activity?','11d4','Regulatory Action')}
  ${discRow('(D5) Has any such agency ever <strong>denied, suspended, or revoked</strong> your registration or license, or otherwise prevented you from associating with an investment-related business or restricted your activities?','11d5','Regulatory Action')}
`,'11d')}

${sub('11E','Self-Regulatory Organization (SRO) Actions',`
  <div class="alert alert-info"><div class="alert-icon">📄</div><div class="alert-body"><strong>Regulatory Action DRP required for any "Yes"</strong></div></div>
  ${discRow('(E1) Has any SRO or commodities exchange ever found you or any advisory affiliate to have <strong>made a false statement or omission</strong>?','11e1','Regulatory Action')}
  ${discRow('(E2) Has any SRO or commodities exchange ever found you or any advisory affiliate to have been involved in a <strong>violation of its rules</strong> (other than a "minor rule violation" under an SEC-approved plan)?','11e2','Regulatory Action')}
  ${discRow('(E3) Has any SRO or commodities exchange ever found you or any advisory affiliate to have been the cause of an investment-related business having its authorization to do business <strong>denied, suspended, revoked, or restricted</strong>?','11e3','Regulatory Action')}
  ${discRow('(E4) Has any SRO or commodities exchange ever <strong>disciplined you or any advisory affiliate</strong> by expelling, suspending, barring, or otherwise restricting your activities?','11e4','Regulatory Action')}
`,'11e')}

${sub('11F–H','Professional Authorizations & Civil Actions',`
  <div class="alert alert-info"><div class="alert-icon">📄</div><div class="alert-body"><strong>Regulatory Action DRP required for 11F–G "Yes" answers; Civil Judicial Action DRP required for 11H "Yes" answers</strong></div></div>
  ${discRow('(F) Has an authorization to act as an <strong>attorney, accountant, or federal contractor</strong> granted to you or any advisory affiliate ever been <strong>revoked or suspended</strong>?','11f','Regulatory Action')}
  ${discRow('(G) Are you or any advisory affiliate now the <strong>subject of any regulatory proceeding</strong> that could result in a "Yes" to any part of Items 11C, 11D, or 11E?','11g','Regulatory Action')}
  <hr class="divider">
  ${discRow('(H1a) In the past 10 years, has any domestic or foreign court <strong>enjoined you or any advisory affiliate</strong> in connection with any investment-related activity?','11h1a','Civil Judicial Action')}
  ${discRow('(H1b) Has any domestic or foreign court ever found that you or any advisory affiliate were <strong>involved in a violation of investment-related statutes or regulations</strong>?','11h1b','Civil Judicial Action')}
  ${discRow('(H1c) Has any domestic or foreign court ever <strong>dismissed an investment-related civil action</strong> pursuant to a settlement agreement (brought by a state or foreign financial regulatory authority)?','11h1c','Civil Judicial Action')}
  ${discRow('(H2) Are you or any advisory affiliate now the subject of any <strong>civil proceeding</strong> that could result in a "Yes" to any part of Item 11H(1)?','11h2','Civil Judicial Action')}
`,'11fh')}`
},

// ─────────────── SECTION 12: SMALL BUSINESSES ───────────────
{ id:'item12', short:'Item 12 — Small Businesses', item:'Item 12', title:'Small Business Regulatory Flexibility',
  subtitle:'Required by the Regulatory Flexibility Act for SEC-registered advisers with RAUM under $25 million.',
  icon:'🏪',
  html:`
  ${alert_('info','📏','Who must complete Item 12','Answer this item only if you are registered or registering with the SEC AND your RAUM (Item 5F(2)(c)) is less than $25 million. Skip if you are filing for initial state registration, amending a current state registration, or switching from SEC to state registration.')}
  ${alert_('info','💡','Key definitions for this item','"Total Assets" = your firm\'s own total assets (not client AUM). "Control" = power to direct management or policies (25%+ voting rights or profits creates a presumption of control).')}

${sub('12A','Firm Total Assets',`
  <div class="fg">
    ${field('Did your firm have <strong>total assets of $5 million or more</strong> on the last day of your most recently completed fiscal year?','12A',yn('total-assets-5m'),'Use total assets on your firm\'s balance sheet — not RAUM. If yes, skip Items 12B and 12C.',true,'If your firm has $5M+ in total assets, it is not a "small entity" under the Regulatory Flexibility Act and no further Item 12 responses are needed.')}
  </div>
`,'12a')}

${sub('12B','Control of Other Entities',`
  <div class="fg">
    ${discRow('(1) Do you <strong>control</strong> another investment adviser that had RAUM of $25 million or more on the last day of its most recently completed fiscal year?','12b1',null)}
    ${discRow('(2) Do you <strong>control</strong> another person (other than a natural person) that had total assets of $5 million or more on the last day of its most recently completed fiscal year?','12b2',null)}
  </div>
`,'12b')}

${sub('12C','Controlled By / Under Common Control',`
  <div class="fg">
    ${discRow('(1) Are you <strong>controlled by or under common control with</strong> another investment adviser that had RAUM of $25 million or more on the last day of its most recently completed fiscal year?','12c1',null)}
    ${discRow('(2) Are you <strong>controlled by or under common control with</strong> another person (other than a natural person) that had total assets of $5 million or more on the last day of its most recently completed fiscal year?','12c2',null)}
  </div>
`,'12c')}`
},

// ─────────────── SECTION 13: SIGNATURE ───────────────
{ id:'item-sig', short:'Signatures & Certification', item:'Signatures', title:'Signatures & Certification',
  subtitle:'Review, certify, and sign your Form ADV Part 1A submission.',
  icon:'✍️',
  html:`
  ${alert_('error','🚨','Legal warning','Complete this form truthfully. False statements or omissions may result in denial of your application, revocation of your registration, or criminal prosecution. You must keep this form updated by filing periodic amendments.')}

${sub('Sig','Authorized Signatory',`
  <div class="fg fg-2">
    ${field('Full legal name of authorized signatory','',inp('text','Last, First, Middle'),'',true,'The person executing this filing must be authorized to bind the investment adviser — typically the CCO, CEO, or Managing Member.')}
    ${field('Title or position','',inp('text','e.g. Chief Compliance Officer, Managing Member'),'',true)}
    ${field('Signature date','',inp('date',''),'',true)}
    ${field('Telephone number','',inp('tel','(000) 000-0000'),'',true)}
    ${field('Email address','',inp('email',''),'',true)}
  </div>
  <div style="margin-top:16px;">
    ${field('Electronic signature — type your full legal name exactly','',inp('text','Type your full legal name as your electronic signature'),'By typing your name, you are providing an electronic signature with the same legal effect as a handwritten signature.',true,'Your typed name must exactly match the "Full legal name" field above.')}
  </div>
`,'sig-person')}

${sub('Contact','Filing Contact Person',`
  ${alert_('info','ℹ️','Optional but recommended','Provide a contact for any follow-up questions from IARD staff or state regulators about this filing.')}
  <div class="fg fg-2">
    ${field('Contact person name','',inp('text',''),'','','',true)}
    ${field('Contact email','',inp('email',''),'','','',true)}
    ${field('Contact telephone','',inp('tel','(000) 000-0000'),'','','',true)}
    ${field('Contact fax','',inp('tel','(000) 000-0000'),'','','',true)}
  </div>
`,'sig-contact')}

${sub('Cert','Final Certification',`
  <div class="cert-box" id="cert-box">
    <div class="cert-text">
      "I, the undersigned, pursuant to the requirements of Section 203 of the Investment Advisers Act of 1940 and Rule 204-1 thereunder, hereby file this Form ADV and certify that the information submitted is current, true, and complete to the best of my knowledge and belief. I further certify that any information previously submitted that is not superseded by information submitted on this Form is still current, true, and complete."
    </div>
    <label class="cert-check-row" id="certify-label">
      <input type="checkbox" id="certify-check" onchange="handleCertify(this)">
      <span class="cert-check-label">I have read and certify the above statement. I am authorized to execute this filing on behalf of the investment adviser named in Item 1A.</span>
    </label>
  </div>
`,'sig-cert')}`
}

]; // end SECTIONS

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// DYNAMIC ENTRY BUILDERS
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
function addEntry(listId, label, innerHtml) {
  entryCounters[listId] = (entryCounters[listId] || 0) + 1;
  const n = entryCounters[listId];
  const d = document.createElement('div');
  d.className = 'entry-card';
  d.innerHTML = `<div class="entry-card-hd">
    <span>${label} #${n}</span>
    <div class="entry-card-actions">
      <button class="entry-del" onclick="this.closest('.entry-card').remove()">Remove</button>
    </div>
  </div><div class="entry-body">${innerHtml}</div>`;
  document.getElementById(listId).appendChild(d);
}

function addWebsite() {
  addEntry('websites-list', 'Website / Social Media Account', `
    <div class="fg fg-2">
      ${field('URL / Address','',inp('url','https://www.example.com'),'',true)}
      ${field('Platform type','',sel(['Firm Website','LinkedIn','Twitter / X','Facebook','Instagram','YouTube','Other']),'',true)}
    </div>`);
}

function addPrivateFund() {
  const n = (entryCounters['pf-list'] = (entryCounters['pf-list']||0)+1);
  addEntry('pf-list', 'Private Fund', `
    <div class="fg fg-2">
      ${field('Fund name or anonymization code','',inp('text',''),'If anonymized per Rule 204-2(d), use same code as in your books.',true,'You may use a code to preserve the anonymity of private fund clients.')}
      ${field('Private Fund ID Number (PFID)','',inp('text','805-XXXXXXXX'),'Assigned by IARD. Leave blank for new funds.',false,'',true)}
      ${field('Fund type','',sel(['Hedge Fund','Private Equity Fund','Venture Capital Fund','Real Estate Fund','BDC','Other Private Fund']),'',true)}
      ${field('Fund legal organization','',sel(['LP','LLC','Trust','Corporation','Other']),'',true)}
      ${field('State/country of organization','',inp('text','e.g. Delaware, Cayman Islands'),'',true)}
      ${field('Date of formation','',inp('date',''),'','','',true)}
      ${field('Gross assets (USD)','',addon(inp('number','0','min=0 step=1000'),'USD'),'As of most recently completed fiscal year.',true)}
      ${field('Net assets (USD)','',addon(inp('number','0','min=0 step=1000'),'USD'),'',true)}
      ${field('Number of investors','',inp('number','0','min=0'),'Approximate.',true)}
      ${field('Is this fund a fund-of-funds?','',yn(`pf-fof-${n}`),'',false)}
      ${field('Are you the primary adviser for this fund (file 7B(1))? If no, you are a sub-adviser (file 7B(2)).','',yn(`pf-primary-${n}`),'',true)}
    </div>`);
}

function addSchedA() {
  const n = (entryCounters['sched-a-list'] = (entryCounters['sched-a-list']||0)+1);
  addEntry('sched-a-list', 'Direct Owner / Executive Officer', `
    <div class="fg fg-2">
      ${field('Full legal name','',inp('text','Last, First, Middle for individuals'),'',true)}
      ${field('Entity type','',sel([['DE','DE — Domestic Entity'],['FE','FE — Foreign Entity'],['I','I — Individual']]),'',true,'DE = domestic entity; FE = entity incorporated or domiciled in a foreign country; I = individual')}
      ${field('Title or Status','',inp('text','e.g. CEO, Shareholder (Class A), General Partner'),'',true,'Include board/management titles; status as partner, trustee, sole proprietor, elected manager, shareholder, or member; and for shareholders/members, the class of securities owned.')}
      ${field('Date title/status acquired','',inp('text','MM/YYYY'),'',true)}
      ${field('Ownership code','',sel([['NA','NA — Less than 5%'],['A','A — 5% to less than 10%'],['B','B — 10% to less than 25%'],['C','C — 25% to less than 50%'],['D','D — 50% to less than 75%'],['E','E — 75% or more']]),'',true,'Select the code that reflects this person\'s ownership percentage.')}
      ${field('Is this person a control person?','',yn(`sa-cp-${n}`),'Most executive officers and all 25%+ owners, general partners, elected managers, and trustees are control persons.',true)}
      ${field('Is this a public reporting company (PR)?','',yn(`sa-pr-${n}`),'A company subject to Sections 12 or 15(d) of the Exchange Act.',true)}
      ${field('CRD No. / SS No. & Date of Birth / IRS Tax No. / Employer ID No.','',inp('text',''),'Provide the most applicable identifier.',true,'For individuals: provide CRD number if available; if not, Social Security Number and date of birth. For entities: provide IRS Tax Number or Employer ID Number.')}
    </div>`);
}

function addSchedB() {
  const n = (entryCounters['sched-b-list'] = (entryCounters['sched-b-list']||0)+1);
  addEntry('sched-b-list', 'Indirect Owner', `
    <div class="fg fg-2">
      ${field('Full legal name','',inp('text','Last, First, Middle for individuals'),'',true)}
      ${field('Entity type','',sel([['DE','DE — Domestic Entity'],['FE','FE — Foreign Entity'],['I','I — Individual']]),'',true)}
      ${field('Status','',inp('text','e.g. Partner, Trustee, Member, Shareholder'),'',true)}
      ${field('Date status acquired','',inp('text','MM/YYYY'),'',true)}
      ${field('Ownership code','',sel([['NA','NA — Less than 5%'],['A','A — 5% to less than 10%'],['B','B — 10% to less than 25%'],['C','C — 25% to less than 50%'],['D','D — 50% to less than 75%'],['E','E — 75% or more']]),'',true)}
      ${field('Is this person a control person?','',yn(`sb-cp-${n}`),'',true)}
      ${field('Is this a public reporting company (PR)?','',yn(`sb-pr-${n}`),'',true)}
      ${field('CRD No. / IRS Tax No. / EIN','',inp('text',''),'',true)}
      ${field('Name of the Schedule A entity that this person indirectly owns','',inp('text','Enter entity name from Schedule A'),'',true,'List the direct owner from Schedule A that this indirect owner controls.')}
    </div>`);
}

function addAuditor() {
  addEntry('auditors-list', 'Accountant / Auditor', `
    <div class="fg fg-2">
      ${field('Name of accounting firm','',inp('text',''),'',true)}
      ${field('PCAOB registration number','',inp('text',''),'If firm is PCAOB-registered.',false,'',true)}
      ${field('City','',inp('text',''),'',true)} ${field('State','',sel(STATES),'',true)}
      ${field('Role','',sel([['2','Annual Audit (9C(2))'],['3','Surprise Examination (9C(3))'],['4','Internal Control Report (9C(4))']],'Select role'),'',true,'Select the type of engagement this accountant performs.')}
    </div>`);
}

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// NAV & SECTION RENDERING
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
const NAV_GROUPS = [
  { label: 'Setup', range: [0,0] },
  { label: 'Registration', range: [1,3] },
  { label: 'Business Information', range: [4,6] },
  { label: 'Affiliations & Transactions', range: [7,9] },
  { label: 'Ownership & Disclosures', range: [10,12] },
  { label: 'Final Submission', range: [13,13] }
];

function buildNav() {
  const list = document.getElementById('nav-list');
  let html = '';
  NAV_GROUPS.forEach(g => {
    html += `<div class="nav-group-label">${g.label}</div>`;
    for (let i = g.range[0]; i <= g.range[1]; i++) {
      const s = SECTIONS[i];
      html += `<div class="nav-item" id="navi-${i}" onclick="goTo(${i})">
        <div class="nav-badge" id="nbadge-${i}"><span class="nav-badge-num">${i+1}</span></div>
        <div class="nav-label" id="nlabel-${i}">${s.short}</div>
      </div>`;
    }
  });
  list.innerHTML = html;
}

function buildSections() {
  const mc = document.getElementById('main-content');
  mc.innerHTML = SECTIONS.map((s,i) => `
    <div class="form-section ${i===0?'active':''}" id="fs-${i}">
      <div class="section-hd">
        <div class="section-hd-left">
          <div class="section-eyebrow">
            <span class="eyebrow-tag">${s.icon} ${s.item}</span>
          </div>
          <h1 class="section-title">${s.title}</h1>
          <div class="section-subtitle">${s.subtitle}</div>
        </div>
        <div class="section-completion">
          <div class="completion-pct" id="cpct-${i}">—</div>
          <div class="completion-label">section filled</div>
        </div>
      </div>
      ${s.html}
      <div class="section-nav">
        <button class="nav-btn nav-btn-back" onclick="goTo(${i-1})" ${i===0?'style="visibility:hidden"':''}>← Back</button>
        <div class="nav-section-info">
          <div class="nav-section-num">${i+1} of ${SECTIONS.length}</div>
          ${i < SECTIONS.length-1 ? `<div class="nav-section-name">Next: ${SECTIONS[i+1].short}</div>` : ''}
        </div>
        ${i < SECTIONS.length-1
          ? `<button class="nav-btn nav-btn-next" onclick="goTo(${i+1})">Continue →</button>`
          : `<button class="nav-btn nav-btn-submit" onclick="submitForm()">Submit Filing ✓</button>`}
      </div>
    </div>`).join('') + `
  <div class="form-section" id="fs-success">
    <div class="success-wrap">
      <div class="success-icon-big">✓</div>
      <h2>Filing Prepared Successfully</h2>
      <p>Your Form ADV Part 1A has been completed. The next step is to submit it through the SEC's IARD system.</p>
      <p style="margin-top:8px;">Remember to complete any required <strong>Disclosure Reporting Pages (DRPs)</strong> in IARD for each "Yes" answer in Item 11, and all required <strong>Schedule D</strong> sections.</p>
      <div class="success-checklist">
        <h4>Pre-Submission Checklist</h4>
        <ul>
          <li>Review all responses with your CCO and legal counsel</li>
          <li>Complete all required Schedule D sections in IARD</li>
          <li>Prepare DRPs for any Item 11 "Yes" disclosures</li>
          <li>Pay the applicable IARD filing fee</li>
          <li>Submit via IARD at iard.com</li>
          <li>Retain a copy of the filed form for your records</li>
          <li>Set a reminder for your next annual update deadline</li>
        </ul>
      </div>
      <div class="success-actions">
        <button class="nav-btn nav-btn-next" onclick="exportSummary()">⬇ Download Summary</button>
        <button class="nav-btn nav-btn-back" onclick="goTo(0)">← Review Form</button>
        <button class="nav-btn nav-btn-submit" onclick="location.reload()">Start New Filing</button>
      </div>
    </div>
  </div>`;
}

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// NAVIGATION
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
function goTo(i) {
  if (i < 0) return;
  // deactivate current
  document.getElementById(`fs-${currentIdx}`)?.classList.remove('active');
  document.getElementById(`navi-${currentIdx}`)?.classList.remove('active');
  // mark prev as completed if going forward
  if (i > currentIdx) {
    const nb = document.getElementById(`nbadge-${currentIdx}`);
    if (nb) { nb.innerHTML = '✓'; nb.style.background = 'var(--green)'; nb.style.color = 'white'; nb.style.borderColor = 'var(--green)'; }
    document.getElementById(`navi-${currentIdx}`)?.classList.add('completed');
  }
  currentIdx = i;
  // show success or section
  if (i >= SECTIONS.length) {
    document.getElementById('fs-success').classList.add('active');
    document.getElementById('pgbar').style.width = '100%';
    document.getElementById('overall-fill').style.width = '100%';
    document.getElementById('pct-label').textContent = '100%';
    return;
  }
  document.getElementById(`fs-${i}`).classList.add('active');
  document.getElementById(`navi-${i}`)?.classList.add('active');
  updateProgress();
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function updateProgress() {
  const pct = Math.round((currentIdx / SECTIONS.length) * 100);
  document.getElementById('pgbar').style.width = pct + '%';
  document.getElementById('overall-fill').style.width = pct + '%';
  document.getElementById('pct-label').textContent = pct + '%';
}

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// INTERACTIVE HELPERS
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
function toggleSub(hdr) {
  hdr.classList.toggle('collapsed');
  const sid = hdr.id.replace('ssh-','');
  const body = document.getElementById('ss-body-' + sid);
  if (body) body.classList.toggle('hidden');
}

function setYN(btn) {
  const name = btn.dataset.name;
  const val = btn.dataset.val;
  // update hidden input
  const hidden = btn.closest('.yn-toggle').querySelector('.yn-hidden');
  if (hidden) hidden.value = val;
  // style buttons
  const all = btn.closest('.yn-toggle').querySelectorAll('.yn-btn');
  all.forEach(b => { b.classList.remove('sel-yes','sel-no'); });
  btn.classList.add(val === 'yes' ? 'sel-yes' : 'sel-no');
  // handle conditional reveals
  const cond = document.getElementById('cond-' + name);
  if (cond) cond.classList.toggle('show', val === 'yes');
  // handle DRP notices for Item 11
  const drow = document.getElementById('drow-' + name);
  if (drow) {
    drow.classList.toggle('disc-yes', val === 'yes');
    const drp = document.getElementById('drp-' + name);
    if (drp) drp.classList.toggle('show', val === 'yes');
  }
  // handle 9A custody reveal
  if ((name === '9a1a' || name === '9a1b') && val === 'yes') {
    document.getElementById('cond-9a')?.classList.add('show');
  }
  if ((name === '9b1a' || name === '9b1b') && val === 'yes') {
    document.getElementById('cond-9b')?.classList.add('show');
  }
  // certify box
  if (name === 'certify') {
    const box = document.getElementById('cert-box');
    if (box) box.classList.toggle('cert-signed', val === 'yes');
  }
}

function handleCertify(cb) {
  document.getElementById('cert-box').classList.toggle('cert-signed', cb.checked);
}

function toggleClass(el, fromCls, toggleCls) {
  el.classList.toggle(toggleCls);
}

function selOpt(el) {
  // For radio groups inside opt-list, ensure only one sel at a time
  const name = el.querySelector('input')?.name;
  if (!name) return;
  document.querySelectorAll(`input[name="${name}"]`).forEach(inp => {
    inp.closest('.opt-item')?.classList.remove('sel');
  });
  el.classList.add('sel');
  // trigger conditional (e.g. asset-range, org-type)
}

// State grid functions
function toggleState(chip, name, val) {
  chip.classList.toggle('sel');
  chip.querySelector('input').checked = chip.classList.contains('sel');
  updateStateCount(name);
}

function toggleAllStates(name, sel_) {
  document.querySelectorAll(`#sg-${name} .state-chip`).forEach(c => {
    c.classList.toggle('sel', sel_);
    c.querySelector('input').checked = sel_;
  });
  updateStateCount(name);
}

function filterStates(inp_, name) {
  const q = inp_.value.toUpperCase();
  document.querySelectorAll(`#sg-${name} .state-chip`).forEach(c => {
    c.style.display = c.textContent.includes(q) ? '' : 'none';
  });
}

function updateStateCount(name) {
  const count = document.querySelectorAll(`#sg-${name} .state-chip.sel`).length;
  const el = document.getElementById('ss-' + name);
  if (el) el.innerHTML = count === 0 ? 'No states selected' : `<strong>${count} state${count!==1?'s':''} selected</strong>`;
}

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// SAVE / EXPORT / SUBMIT
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
function saveProgress() {
  const b = document.querySelector('.hdr-btn-gold');
  const orig = b.innerHTML;
  b.innerHTML = '✓ Saved!';
  b.style.background = 'var(--green)';
  b.style.color = 'white';
  setTimeout(() => { b.innerHTML = orig; b.style.background = ''; b.style.color = ''; }, 2200);
}

function exportSummary() {
  alert('In a production deployment, this would generate a PDF summary of your responses for attorney review before IARD submission.');
}

function showHelp() {
  alert('Form ADV Part 1A Help\n\n• Fields marked * are required\n• Hover the ? icons for field-specific guidance\n• "Yes" answers to Item 11 questions require DRPs in IARD\n• Use "Save Draft" frequently\n• Submit the completed form through IARD at www.iard.com\n• Annual updates due within 90 days of fiscal year end\n\nFor official instructions: sec.gov/info/edgar/forms/formadv.pdf');
}

function submitForm() {
  const cb = document.getElementById('certify-check');
  if (!cb || !cb.checked) {
    alert('Please check the certification box in the Signatures section before submitting.');
    return;
  }
  goTo(SECTIONS.length);
}

// Radio/checkbox interaction
document.addEventListener('change', e => {
  if (e.target.type === 'checkbox' || e.target.type === 'radio') {
    const p = e.target.closest('.opt-item');
    if (p && e.target.type === 'checkbox') p.classList.toggle('sel', e.target.checked);
  }
});

// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// INIT
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
buildNav();
buildSections();
updateProgress();

// Activate first nav item
document.getElementById('navi-0')?.classList.add('active');
</script>
</body>
</html>
