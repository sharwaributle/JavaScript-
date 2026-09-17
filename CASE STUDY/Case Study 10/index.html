// Store student data
let students = [];


// ======================================
// DISPLAY STUDENTS
// ======================================

function displayStudents(data) {

    const table = document.getElementById("studentTable");

    table.innerHTML = "";


    // No matching students
    if (data.length === 0) {

        table.innerHTML = `
            <tr>
                <td colspan="6" class="empty">
                    No student matches the search/filter criteria.
                </td>
            </tr>
        `;

        document.getElementById("message").innerText =
            "No students found.";

        return;
    }


    document.getElementById("message").innerText =
        data.length + " student(s) found.";


    // Generate table rows
    data.forEach(student => {

        const row = document.createElement("tr");

        const status =
            student.registrationStatus.toLowerCase();

        row.innerHTML = `

            <td>
                <strong>${student.studentName}</strong>
            </td>

            <td>
                ${student.prn}
            </td>

            <td>
                ${student.department}
            </td>

            <td>
                ${student.year}
            </td>

            <td>
                ${student.eventName}
            </td>

            <td>
                <span class="status ${status}">
                    ${student.registrationStatus}
                </span>
            </td>

        `;

        table.appendChild(row);

    });

}


// ======================================
// UPDATE STATISTICS
// ======================================

function updateStatistics() {

    const total = students.length;

    const registered =
        students.filter(
            student =>
                student.registrationStatus === "Registered"
        ).length;

    const pending =
        students.filter(
            student =>
                student.registrationStatus === "Pending"
        ).length;

    const cancelled =
        students.filter(
            student =>
                student.registrationStatus === "Cancelled"
        ).length;


    document.getElementById("totalCount")
        .innerText = total;

    document.getElementById("registeredCount")
        .innerText = registered;

    document.getElementById("pendingCount")
        .innerText = pending;

    document.getElementById("cancelledCount")
        .innerText = cancelled;
}


// ======================================
// FETCH API
// ======================================

document
    .getElementById("loadBtn")
    .addEventListener("click", function () {

        fetch("students.json")

            .then(response => {

                if (!response.ok) {

                    throw new Error(
                        "JSON file could not be loaded"
                    );

                }

                return response.json();

            })

            .then(data => {

                students = data;

                updateStatistics();

                displayStudents(students);

            })

            .catch(error => {

                document.getElementById("message")
                    .innerText =
                    "❌ JSON data cannot be loaded.";

                console.log(error);

            });

    });


// ======================================
// JQUERY $.getJSON()
// ======================================

$("#jqueryBtn").click(function () {

    $.getJSON("students.json")

        .done(function (data) {

            students = data;

            updateStatistics();

            displayStudents(students);

        })

        .fail(function () {

            $("#message").text(
                "❌ JSON data cannot be loaded."
            );

        });

});


// ======================================
// SEARCH
// ======================================

$("#searchBox").on("keyup", function () {

    filterStudents();

});


// ======================================
// STATUS FILTER
// ======================================

$("#statusFilter").on("change", function () {

    filterStudents();

});


// ======================================
// FILTER FUNCTION
// ======================================

function filterStudents() {

    const searchText =
        $("#searchBox")
            .val()
            .toLowerCase();

    const selectedStatus =
        $("#statusFilter").val();


    const filteredStudents =
        students.filter(student => {

            const name =
                student.studentName.toLowerCase();

            const prn =
                student.prn.toLowerCase();


            const matchesSearch =
                name.includes(searchText) ||
                prn.includes(searchText);


            const matchesStatus =
                selectedStatus === "All" ||
                student.registrationStatus ===
                selectedStatus;


            return matchesSearch && matchesStatus;

        });


    displayStudents(filteredStudents);

}


// ======================================
// DARK / LIGHT MODE
// ======================================

const themeBtn =
    document.getElementById("themeBtn");


// Check saved theme
const savedTheme =
    localStorage.getItem("theme");

if (savedTheme === "dark") {

    document.body.classList.add("dark");

    themeBtn.innerText = "☀️ Light";

}


// Theme button
themeBtn.addEventListener("click", function () {

    document.body.classList.toggle("dark");


    if (document.body.classList.contains("dark")) {

        themeBtn.innerText = "☀️ Light";

        localStorage.setItem(
            "theme",
            "dark"
        );

    } else {

        themeBtn.innerText = "🌙 Dark";

        localStorage.setItem(
            "theme",
            "light"
        );

    }

});
