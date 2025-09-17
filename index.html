<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Notepad Pro</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #181818;
            --surface-color: #212121;
            --primary-text-color: #e0e0e0;
            --secondary-text-color: #a0a0a0;
            --primary-color: #3f51b5;
            --accent-color: #03dac6;
            --danger-color: #cf6679;
            --border-color: #333333;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--primary-text-color);
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        .hidden { display: none !important; }
        
        /* --- Views Container --- */
        .view { max-width: 650px; margin: auto; }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 16px;
            background-color: var(--surface-color);
            position: sticky; top: 0; z-index: 10;
            border-bottom: 1px solid var(--border-color);
        }

        header h1 { font-size: 1.1rem; font-weight: 700; }
        
        .icon-btn {
            background: none; border: none; cursor: pointer;
            color: var(--secondary-text-color); padding: 8px;
            border-radius: 50%; display: flex; align-items: center; justify-content: center;
            transition: background-color 0.2s ease, color 0.2s ease;
        }
        .icon-btn:hover { background-color: rgba(255, 255, 255, 0.1); color: var(--primary-text-color); }
        .icon { width: 22px; height: 22px; stroke-width: 2; }
        
        .header-actions { display: flex; align-items: center; gap: 8px; }
        .text-btn { font-size: 0.9rem; font-weight: 700; color: var(--accent-color); background: none; border: none; cursor: pointer; padding: 8px 12px; border-radius: 5px; transition: background-color 0.2s ease; }
        .text-btn:hover { background-color: rgba(3, 218, 202, 0.1); }
        .text-btn.delete { color: var(--danger-color); }
        .text-btn.delete:hover { background-color: rgba(207, 102, 121, 0.1); }

        .search-container { padding: 8px 16px; background-color: var(--surface-color); }
        #search-input { width: 100%; padding: 12px; background-color: #333; border: 1px solid #444; border-radius: 8px; color: var(--primary-text-color); font-size: 1rem; transition: border-color 0.2s ease, box-shadow 0.2s ease; }
        #search-input:focus { outline: none; border-color: var(--accent-color); box-shadow: 0 0 0 2px rgba(3, 218, 202, 0.3); }

        .notes-list-container { padding: 16px; }
        .note-item {
            background-color: var(--surface-color); padding: 16px; border-radius: 10px; margin-bottom: 12px;
            cursor: pointer; transition: transform 0.2s ease, box-shadow 0.2s ease; border: 1px solid var(--border-color);
        }
        .note-item:hover { transform: translateY(-3px); box-shadow: 0 4px 15px rgba(0,0,0,0.2); }
        .note-item h3 { font-size: 1.1rem; margin-bottom: 8px; }
        .note-item .note-content-preview { font-size: 0.9rem; color: var(--secondary-text-color); line-height: 1.6; max-height: 60px; overflow: hidden; }
        .note-item .note-timestamp { font-size: 0.8rem; color: #888; margin-top: 12px; }

        /* Checklist Styles */
        .checklist-item { display: flex; align-items: center; margin: 8px 0; }
        .checklist-item-box { width: 18px; height: 18px; border: 2px solid var(--secondary-text-color); border-radius: 4px; margin-right: 12px; display: inline-block; cursor: pointer; transition: all 0.2s ease; }
        .checklist-item.checked .checklist-item-box { background-color: var(--accent-color); border-color: var(--accent-color); }
        .checklist-item.checked .checklist-item-text { text-decoration: line-through; color: var(--secondary-text-color); }

        #add-note-fab {
            position: fixed; bottom: 30px; right: 30px; width: 56px; height: 56px; background-color: var(--accent-color);
            color: #000; border-radius: 16px; border: none; cursor: pointer; display: flex; justify-content: center;
            align-items: center; box-shadow: 0 6px 20px rgba(3, 218, 202, 0.3); transition: transform 0.2s ease, box-shadow 0.2s ease;
        }
        #add-note-fab:hover { transform: scale(1.05); box-shadow: 0 8px 25px rgba(3, 218, 202, 0.4); }
        
        /* --- Editor View --- */
        .editor-container { display: flex; flex-direction: column; height: calc(100vh - 61px); }
        #note-title-input, #note-content-input {
            background-color: var(--bg-color); color: var(--primary-text-color); border: none; padding: 16px; width: 100%;
        }
        #note-title-input { font-size: 1.5rem; font-weight: 700; }
        #note-content-input { flex-grow: 1; font-size: 1rem; line-height: 1.7; resize: none; }
        #note-title-input:focus, #note-content-input:focus { outline: none; }

        /* --- Trash View --- */
        .trash-actions { margin-top: 15px; display: flex; gap: 10px; }
        .trash-actions button { font-size: 0.9rem; padding: 6px 10px; }

        /* --- Dropdown Menu --- */
        .dropdown { position: relative; display: inline-block; }
        .dropdown-content {
            display: none; position: absolute; right: 0; background-color: #2c2c2c; min-width: 220px;
            box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.3); z-index: 1; border-radius: 8px;
            overflow: hidden; transform-origin: top right;
            animation: dropdown-scale 0.2s ease-out;
        }
        .dropdown-content button {
            color: var(--primary-text-color); padding: 12px 16px; display: block; width: 100%;
            text-align: left; background: none; border: none; cursor: pointer; font-size: 0.9rem;
        }
        .dropdown-content button:hover { background-color: #3f3f3f; }
        .show { display: block; }
        @keyframes dropdown-scale { from { opacity: 0; transform: scale(0.95); } to { opacity: 1; transform: scale(1); } }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: var(--surface-color); }
        ::-webkit-scrollbar-thumb { background: #555; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #777; }
    </style>
</head>
<body>
    <!-- Main View -->
    <div id="main-view" class="view">
        <header>
            <h1>Notepad Pro</h1>
            <div class="header-actions">
                <button id="sort-btn" class="icon-btn" title="Sort Notes">
                    <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" d="M3 4h13M3 8h9m-9 4h6m4 0l4-4m0 0l4 4m-4-4v12"></path></svg>
                </button>
                <div class="dropdown">
                    <button id="more-btn" class="icon-btn" title="More Options">
                        <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z"></path></svg>
                    </button>
                    <div id="more-dropdown" class="dropdown-content">
                        <button id="trash-menu-btn">Trash</button>
                        <hr style="border-color: #444;">
                        <button id="export-btn">Export notes to text file</button>
                        <button id="import-btn-label">Import from text file</button>
                        <input type="file" id="import-file" class="hidden" accept=".txt">
                    </div>
                </div>
            </div>
        </header>
        <div class="search-container"><input type="text" id="search-input" placeholder="Search notes..."></div>
        <div id="notes-list" class="notes-list-container"></div>
        <button id="add-note-fab" title="Add New Note">
            <svg class="icon" style="width: 28px; height: 28px;" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" d="M12 6v6m0 0v6m0-6h6m-6 0H6"></path></svg>
        </button>
    </div>

    <!-- Editor View -->
    <div id="editor-view" class="view hidden">
        <header>
            <button id="back-btn" class="icon-btn" title="Back">
                <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" d="M10 19l-7-7m0 0l7-7m-7 7h18"></path></svg>
            </button>
            <div class="header-actions">
                <button id="checklist-helper-btn" class="icon-btn" title="Add Checklist Item">
                     <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                </button>
                <button id="delete-btn" class="text-btn delete">DELETE</button>
                <button id="save-btn" class="text-btn">SAVE</button>
            </div>
        </header>
        <div class="editor-container">
            <input type="text" id="note-title-input" placeholder="Title">
            <textarea id="note-content-input" placeholder="Start writing..."></textarea>
        </div>
    </div>
    
    <!-- Trash View -->
    <div id="trash-view" class="view hidden">
        <header>
            <button id="trash-back-btn" class="icon-btn" title="Back to Notes">
                <svg class="icon" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" d="M10 19l-7-7m0 0l7-7m-7 7h18"></path></svg>
            </button>
            <h1>Trash</h1>
        </header>
        <div id="trash-list" class="notes-list-container"></div>
    </div>

    <script>
        // --- JavaScript Logic (No changes needed, it works with the new design) ---
        document.addEventListener('DOMContentLoaded', () => {
            const mainView = document.getElementById('main-view'), editorView = document.getElementById('editor-view'), trashView = document.getElementById('trash-view'), notesList = document.getElementById('notes-list'), trashList = document.getElementById('trash-list'), addNoteFab = document.getElementById('add-note-fab'), backBtn = document.getElementById('back-btn'), saveBtn = document.getElementById('save-btn'), deleteBtn = document.getElementById('delete-btn'), noteTitleInput = document.getElementById('note-title-input'), noteContentInput = document.getElementById('note-content-input'), searchInput = document.getElementById('search-input'), sortBtn = document.getElementById('sort-btn'), moreBtn = document.getElementById('more-btn'), moreDropdown = document.getElementById('more-dropdown'), exportBtn = document.getElementById('export-btn'), importBtnLabel = document.getElementById('import-btn-label'), importFile = document.getElementById('import-file'), trashMenuBtn = document.getElementById('trash-menu-btn'), trashBackBtn = document.getElementById('trash-back-btn'), checklistHelperBtn = document.getElementById('checklist-helper-btn');
            let notes = JSON.parse(localStorage.getItem('notes-pro')) || [], currentNoteId = null, sortOrder = localStorage.getItem('notes-sort-order') || 'date-desc';
            const saveNotes = () => localStorage.setItem('notes-pro', JSON.stringify(notes));
            const parseContentForDisplay = content => content.replace(/^(?:\[ \]|\[x\]) (.*)/gm, (match, text, offset) => `<div class="checklist-item ${match.startsWith('[x]')?'checked':''}" data-line="${offset}"><span class="checklist-item-box"></span><span class="checklist-item-text">${text}</span></div>`).replace(/\n/g, '<br>');
            const renderNotes = () => {
                notesList.innerHTML = ''; const activeNotes = notes.filter(n => !n.isTrashed);
                const sortedNotes = [...activeNotes].sort((a,b) => { switch (sortOrder) { case 'title-asc': return a.title.localeCompare(b.title); case 'title-desc': return b.title.localeCompare(a.title); case 'date-asc': return a.lastEdited - b.lastEdited; default: return b.lastEdited - a.lastEdited; } });
                const searchTerm = searchInput.value.toLowerCase();
                const filteredNotes = sortedNotes.filter(note => note.title.toLowerCase().includes(searchTerm) || note.content.toLowerCase().includes(searchTerm));
                if (filteredNotes.length === 0) { notesList.innerHTML = `<p style="text-align:center; color: var(--secondary-text-color);">No notes. Tap '+' to create one.</p>`; return; }
                filteredNotes.forEach(note => {
                    const item = document.createElement('div'); item.className = 'note-item'; item.dataset.id = note.id;
                    const date = new Date(note.lastEdited).toLocaleString('en-US', { month: 'short', day: 'numeric', hour: '2-digit', minute: '2-digit' });
                    item.innerHTML = `<h3>${note.title}</h3><div class="note-content-preview">${parseContentForDisplay(note.content.substring(0, 150))}</div><p class="note-timestamp">Last edit: ${date}</p>`;
                    item.addEventListener('click', e => { if (e.target.closest('.checklist-item')) { toggleChecklistItem(note.id, parseInt(e.target.closest('.checklist-item').dataset.line)); } else { openEditor(note.id); } });
                    notesList.appendChild(item);
                });
            };
            const renderTrash = () => {
                trashList.innerHTML = ''; const trashedNotes = notes.filter(n => n.isTrashed);
                if (trashedNotes.length === 0) { trashList.innerHTML = `<p style="text-align:center; color: var(--secondary-text-color);">Trash is empty.</p>`; return; }
                trashedNotes.forEach(note => {
                    const item = document.createElement('div'); item.className = 'note-item';
                    item.innerHTML = `<h3>${note.title}</h3><p>Deleted on: ${new Date(note.lastEdited).toLocaleDateString()}</p><div class="trash-actions"><button class="text-btn restore-btn" data-id="${note.id}">Restore</button><button class="text-btn delete perm-delete-btn" data-id="${note.id}">Delete Permanently</button></div>`;
                    trashList.appendChild(item);
                });
                document.querySelectorAll('.restore-btn').forEach(b => b.addEventListener('click', handleRestore));
                document.querySelectorAll('.perm-delete-btn').forEach(b => b.addEventListener('click', handlePermDelete));
            };
            const showView = viewToShow => { [mainView, editorView, trashView].forEach(v => v.classList.add('hidden')); viewToShow.classList.remove('hidden'); };
            const openEditor = (noteId = null) => {
                currentNoteId = noteId; if (noteId) { const note = notes.find(n => n.id === noteId); noteTitleInput.value = note.title; noteContentInput.value = note.content; deleteBtn.classList.remove('hidden'); } else { noteTitleInput.value = ''; noteContentInput.value = ''; deleteBtn.classList.add('hidden'); }
                showView(editorView); noteTitleInput.focus();
            };
            const handleSave = () => {
                const title = noteTitleInput.value.trim() || 'Untitled Note', content = noteContentInput.value.trim();
                if (currentNoteId) { const note = notes.find(n => n.id === currentNoteId); note.title = title; note.content = content; note.lastEdited = Date.now(); } else { notes.push({ id: Date.now(), title, content, lastEdited: Date.now(), isTrashed: false }); }
                saveNotes(); showView(mainView); renderNotes();
            };
            const handleDelete = () => { if (!currentNoteId) return; const note = notes.find(n => n.id === currentNoteId); if(note) { note.isTrashed = true; note.lastEdited = Date.now(); saveNotes(); showView(mainView); renderNotes(); } };
            const handleRestore = e => { const noteId = parseInt(e.target.dataset.id), note = notes.find(n => n.id === noteId); if(note) note.isTrashed = false; saveNotes(); renderTrash(); };
            const handlePermDelete = e => { const noteId = parseInt(e.target.dataset.id); if (confirm('This note will be deleted forever. Are you sure?')) { notes = notes.filter(n => n.id !== noteId); saveNotes(); renderTrash(); } };
            const toggleChecklistItem = (noteId, lineOffset) => {
                const note = notes.find(n => n.id === noteId); if (!note) return;
                const lineEnd = note.content.substring(lineOffset), line = lineEnd.split('\n')[0];
                if(line.startsWith('[]')) { note.content = note.content.substring(0, lineOffset) + line.replace('[]', '[x]') + lineEnd.substring(line.length); } else if (line.startsWith('[x]')) { note.content = note.content.substring(0, lineOffset) + line.replace('[x]', '[]') + lineEnd.substring(line.length); }
                note.lastEdited = Date.now(); saveNotes(); renderNotes();
            };
            const cycleSortOrder = () => { const orders = ['date-desc', 'date-asc', 'title-asc', 'title-desc']; sortOrder = orders[(orders.indexOf(sortOrder) + 1) % orders.length]; localStorage.setItem('notes-sort-order', sortOrder); alert(`Sorted by: ${sortOrder.replace('-',' ')}`); renderNotes(); };
            const exportNotes = () => { if(notes.filter(n=>!n.isTrashed).length === 0){ alert('No notes to export.'); return; } const fileContent = notes.filter(n=>!n.isTrashed).map(note => `[TITLE]: ${note.title}\n\n${note.content}`).join('\n\n---\n\n'); const blob = new Blob([fileContent], { type: 'text/plain;charset=utf-8' }); const link = document.createElement('a'); link.href = URL.createObjectURL(blob); link.download = `notes_export_${new Date().toISOString().slice(0,10)}.txt`; link.click(); };
            const importNotes = e => { const file = e.target.files[0]; if (!file) return; const reader = new FileReader(); reader.onload = e => { const importedNotesArr = []; const notesRaw = e.target.result.split('\n\n---\n\n'); notesRaw.forEach(noteStr => { const titleMatch = noteStr.match(/^\[TITLE\]: (.*)/); if (titleMatch) { importedNotesArr.push({ id: Date.now() + Math.random(), title: titleMatch[1], content: noteStr.substring(titleMatch[0].length).trim(), lastEdited: Date.now(), isTrashed: false }); } }); if (confirm(`Found ${importedNotesArr.length} notes. Add them to your existing notes?`)) { notes = [...notes, ...importedNotesArr]; saveNotes(); renderNotes(); } }; reader.readAsText(file); e.target.value = ''; };
            addNoteFab.addEventListener('click', () => openEditor());
            backBtn.addEventListener('click', () => { showView(mainView); renderNotes(); });
            trashBackBtn.addEventListener('click', () => { showView(mainView); renderNotes(); });
            saveBtn.addEventListener('click', handleSave); deleteBtn.addEventListener('click', handleDelete); searchInput.addEventListener('input', renderNotes); sortBtn.addEventListener('click', cycleSortOrder); moreBtn.addEventListener('click', e => { moreDropdown.classList.toggle('show'); e.stopPropagation(); });
            exportBtn.addEventListener('click', exportNotes); importBtnLabel.addEventListener('click', () => importFile.click()); importFile.addEventListener('change', importNotes);
            trashMenuBtn.addEventListener('click', () => { showView(trashView); renderTrash(); });
            checklistHelperBtn.addEventListener('click', () => { const pos = noteContentInput.selectionStart; const content = noteContentInput.value; noteContentInput.value = content.substring(0, pos) + '\n[] ' + content.substring(pos); noteContentInput.focus(); noteContentInput.setSelectionRange(pos + 4, pos + 4); });
            window.onclick = () => { if (moreDropdown.classList.contains('show')) moreDropdown.classList.remove('show'); };
            renderNotes();
        });
    </script>
</body>
</html>
