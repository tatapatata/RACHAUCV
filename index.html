<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Racha UCV - Huaraz</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f8f8f8;
      color: #333;
      background-size: cover;
      background-position: center;
    }
    header {
      background: rgba(216,35,42,0.9);
      color: white;
      text-align: center;
      padding: 1rem;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    header img {
      height: 70px;
      margin-bottom: 0.5rem;
    }
    main {
      padding: 1rem;
      max-width: 800px;
      margin: auto;
      background: rgba(255,255,255,0.9);
      border-radius: 10px;
    }
    h2 {
      color: #d8232a;
    }
    .course-list, .week-list {
      margin: 1rem 0;
    }
    .course-item, .week-item {
      background: white;
      border-radius: 8px;
      padding: 0.5rem 1rem;
      margin-bottom: 0.5rem;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    button {
      background: #d8232a;
      color: white;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 6px;
      cursor: pointer;
    }
    button:hover {
      background: #b51e24;
    }
    .progress-bar {
      background: #eee;
      border-radius: 6px;
      overflow: hidden;
      margin-top: 0.5rem;
    }
    .progress {
      background: #d8232a;
      height: 16px;
      width: 0;
    }
    .student-info {
      margin: 1rem 0;
      padding: 1rem;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>
  <header>
    <img src="logo_ucv.png" alt="Logo UCV">
    <h1>Racha Académica UCV - Huaraz</h1>
    <p>Mantén tu racha de 16 semanas completando tus tareas</p>
  </header>
  <main>
    <section class="student-info">
      <h2>👤 Información del estudiante</h2>
      <input type="text" id="studentName" placeholder="Nombre del estudiante" />
      <input type="text" id="studentCycle" placeholder="Ciclo" />
      <input type="text" id="studentCareer" placeholder="Carrera" />
      <button onclick="saveStudentInfo()">Guardar información</button>
      <p id="studentDisplay"></p>
    </section>

    <section>
      <h2>📚 Mis Cursos</h2>
      <input type="text" id="courseInput" placeholder="Nombre del curso" />
      <button onclick="addCourse()">Agregar curso</button>
      <div class="course-list" id="courseList"></div>
    </section>

    <section>
      <h2>✅ Tareas de la Semana</h2>
      <input type="text" id="taskInput" placeholder="Nueva tarea" />
      <select id="courseSelect"></select>
      <button onclick="addTask()">Agregar tarea</button>
      <div class="task-list" id="taskList"></div>

      <div class="progress-bar">
        <div class="progress" id="progressBar"></div>
      </div>
      <p id="progressText">Progreso semanal: 0%</p>
    </section>

    <section>
      <h2>🔥 Racha de Semanas</h2>
      <div class="week-list" id="weekList"></div>
    </section>

    <section>
      <h2>🖼️ Personalizar Fondo</h2>
      <input type="file" id="bgInput" accept="image/*" onchange="setBackground(event)">
    </section>
  </main>

  <script>
    let courses = JSON.parse(localStorage.getItem("courses")) || [];
    let tasks = JSON.parse(localStorage.getItem("tasks")) || [];
    let completedWeeks = JSON.parse(localStorage.getItem("weeks")) || 0;
    let student = JSON.parse(localStorage.getItem("student")) || {};

    function saveData() {
      localStorage.setItem("courses", JSON.stringify(courses));
      localStorage.setItem("tasks", JSON.stringify(tasks));
      localStorage.setItem("weeks", JSON.stringify(completedWeeks));
      localStorage.setItem("student", JSON.stringify(student));
    }

    function saveStudentInfo() {
      student.name = document.getElementById("studentName").value;
      student.cycle = document.getElementById("studentCycle").value;
      student.career = document.getElementById("studentCareer").value;
      saveData();
      renderStudentInfo();
    }

    function renderStudentInfo() {
      const display = document.getElementById("studentDisplay");
      if (student.name || student.cycle || student.career) {
        display.innerText = `${student.name || ''} - Ciclo: ${student.cycle || ''} - Carrera: ${student.career || ''}`;
      }
    }

    function setBackground(event) {
      const file = event.target.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          document.body.style.backgroundImage = `url(${e.target.result})`;
        };
        reader.readAsDataURL(file);
      }
    }

    function renderCourses() {
      const list = document.getElementById("courseList");
      const select = document.getElementById("courseSelect");
      list.innerHTML = "";
      select.innerHTML = "";
      courses.forEach((c, i) => {
        let div = document.createElement("div");
        div.className = "course-item";
        div.innerHTML = `<span>${c}</span> <button onclick="removeCourse(${i})">❌</button>`;
        list.appendChild(div);

        let opt = document.createElement("option");
        opt.value = c;
        opt.textContent = c;
        select.appendChild(opt);
      });
    }

    function addCourse() {
      const input = document.getElementById("courseInput");
      if (input.value && courses.length < 10) {
        courses.push(input.value);
        input.value = "";
        saveData();
        renderCourses();
      }
    }

    function removeCourse(index) {
      courses.splice(index, 1);
      tasks = tasks.filter(t => t.course !== courses[index]);
      saveData();
      renderCourses();
      renderTasks();
    }

    function renderTasks() {
      const list = document.getElementById("taskList");
      list.innerHTML = "";
      let completed = 0;
      tasks.forEach((t, i) => {
        let div = document.createElement("div");
        div.className = "course-item";
        div.innerHTML = `<span>${t.task} - <strong>${t.course}</strong></span> 
                         <input type='checkbox' ${t.done ? "checked" : ""} onchange="toggleTask(${i})">`;
        list.appendChild(div);
        if (t.done) completed++;
      });
      let progress = tasks.length ? Math.round((completed / tasks.length) * 100) : 0;
      document.getElementById("progressBar").style.width = progress + "%";
      document.getElementById("progressText").innerText = `Progreso semanal: ${progress}%`;
      if (progress === 100) {
        completedWeeks = Math.min(16, completedWeeks + 1);
        tasks = [];
        saveData();
        renderWeeks();
        renderTasks();
        alert("🎉 ¡Semana completada! Tu racha ha aumentado.");
      }
    }

    function addTask() {
      const taskInput = document.getElementById("taskInput");
      const courseSelect = document.getElementById("courseSelect");
      if (taskInput.value && courseSelect.value) {
        tasks.push({ task: taskInput.value, course: courseSelect.value, done: false });
        taskInput.value = "";
        saveData();
        renderTasks();
      }
    }

    function toggleTask(index) {
      tasks[index].done = !tasks[index].done;
      saveData();
      renderTasks();
    }

    function renderWeeks() {
      const list = document.getElementById("weekList");
      list.innerHTML = "";
      for (let i = 1; i <= 16; i++) {
        let div = document.createElement("div");
        div.className = "week-item";
        div.innerHTML = i <= completedWeeks ? `✅ Semana ${i}` : `⬜ Semana ${i}`;
        list.appendChild(div);
      }
    }

    renderStudentInfo();
    renderCourses();
    renderTasks();
    renderWeeks();
  </script>
</body>
</html>
