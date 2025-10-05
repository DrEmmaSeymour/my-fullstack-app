<template>
  <div class="app">
    <!-- Body -->
    <div class="body">
      <!-- Sidebar -->
      <aside class="sidebar">
        <h2>Facility Dashboard</h2>
        <p>🏋️ Overview</p>
        <p>📅 Bookings</p>
        <p>💳 Members</p>
        <p>⚙️ Settings</p>
      </aside>

      <!-- Main content -->
      <main class="main">

        <div class="cards">
          <div class="card blue">
            <h3>Active Members</h3>
            <p>1,246</p>
          </div>
          <div class="card green">
            <h3>Bookings Today</h3>
            <p>89</p>
          </div>
          <div class="card red">
            <h3>Pending Approvals</h3>
            <p>12</p>
          </div>
        </div>
      </main>
    </div>

    <!-- Footer -->
    <footer class="footer">
      © 2025 Facility Demo
    </footer>
  </div>
</template>

<script setup>
// no logic needed
</script>

<style scoped>
/* ----------- Layout ----------- */
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background: #f3f4f6;
  font-family: system-ui, sans-serif;
}

/* Body wrapper */
.body {
  display: flex;
  flex: 1;
}

/* Sidebar */
.sidebar {
  width: 220px;
  background: #fff;
  padding: 1.5rem 1rem;
  border-right: 1px solid #e5e7eb;
}
.sidebar h2 {
  color: #1d4ed8;
  font-size: 1.25rem;
  margin-bottom: 1rem;
}
.sidebar p {
  margin: 0.75rem 0;
  color: #374151;
  cursor: pointer;
}
.sidebar p:hover {
  background: #e0e7ff;
  border-radius: 4px;
  padding-left: 4px;
}

/* Main area */
.main {
  flex: 1;
  padding: 2rem;
}

/* Header inside main */
.main-header {
  background: #1d4ed8;
  color: white;
  padding: 1rem 1.5rem;
  border-radius: 8px;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

/* Cards */
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1.5rem;
}
.card {
  background: #fff;
  border-radius: 10px;
  padding: 1.5rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}
.card h3 {
  color: #6b7280;
  font-size: 0.9rem;
  margin-bottom: 0.5rem;
}
.card p {
  font-size: 1.8rem;
  font-weight: bold;
}
.blue p { color: #2563eb; }
.green p { color: #059669; }
.red p { color: #dc2626; }

</style>
