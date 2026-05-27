import { useState } from "react";

const initialTournaments = [
  {
    id: 1,
    name: "BOOYAH CLASH #12",
    mode: "Squad",
    map: "Bermuda",
    date: "২৯ মে, ২০২৬",
    time: "রাত ৯:০০",
    slots: 16,
    filled: 11,
    prize: "৳৫,০০০",
    status: "open",
    entryFee: "FREE",
  },
  {
    id: 2,
    name: "LONE WOLF CUP",
    mode: "Solo",
    map: "Kalahari",
    date: "৩০ মে, ২০২৬",
    time: "সন্ধ্যা ৭:৩০",
    slots: 48,
    filled: 48,
    prize: "৳৩,০০০",
    status: "full",
    entryFee: "FREE",
  },
  {
    id: 3,
    name: "DUO DOMINATION",
    mode: "Duo",
    map: "Purgatory",
    date: "১ জুন, ২০২৬",
    time: "রাত ১০:০০",
    slots: 24,
    filled: 6,
    prize: "৳৪,০০০",
    status: "open",
    entryFee: "FREE",
  },
];

const modeColors = {
  Solo: "#ff4f4f",
  Duo: "#f5a623",
  Squad: "#00e5ff",
};

const mapIcons = {
  Bermuda: "🏝️",
  Kalahari: "🏜️",
  Purgatory: "🌋",
};

export default function App() {
  const [page, setPage] = useState("home");
  const [tournaments, setTournaments] = useState(initialTournaments);
  const [joined, setJoined] = useState([]);
  const [selected, setSelected] = useState(null);
  const [form, setForm] = useState({ name: "", uid: "", phone: "" });
  const [formError, setFormError] = useState("");
  const [successMsg, setSuccessMsg] = useState("");
  const [createForm, setCreateForm] = useState({
    name: "",
    mode: "Squad",
    map: "Bermuda",
    date: "",
    time: "",
    slots: 16,
    prize: "",
  });
  const [tab, setTab] = useState("all");

  const filtered = tab === "joined"
    ? tournaments.filter(t => joined.includes(t.id))
    : tournaments;

  function handleJoinClick(t) {
    setSelected(t);
    setForm({ name: "", uid: "", phone: "" });
    setFormError("");
    setSuccessMsg("");
    setPage("register");
  }

  function handleRegister() {
    if (!form.name || !form.uid || !form.phone) {
      setFormError("সব তথ্য পূরণ করুন!");
      return;
    }
    if (form.uid.length < 6) {
      setFormError("সঠিক UID দিন (কমপক্ষে ৬ সংখ্যা)");
      return;
    }
    setJoined(prev => [...prev, selected.id]);
    setTournaments(prev =>
      prev.map(t =>
        t.id === selected.id ? { ...t, filled: t.filled + 1 } : t
      )
    );
    setSuccessMsg("🎉 রেজিস্ট্রেশন সফল হয়েছে! গুড লাক!");
    setFormError("");
  }

  function handleCreate() {
    if (!createForm.name || !createForm.date || !createForm.time || !createForm.prize) return;
    const newT = {
      id: Date.now(),
      name: createForm.name.toUpperCase(),
      mode: createForm.mode,
      map: createForm.map,
      date: createForm.date,
      time: createForm.time,
      slots: Number(createForm.slots),
      filled: 0,
      prize: `৳${createForm.prize}`,
      status: "open",
      entryFee: "FREE",
    };
    setTournaments(prev => [newT, ...prev]);
    setPage("home");
    setCreateForm({ name: "", mode: "Squad", map: "Bermuda", date: "", time: "", slots: 16, prize: "" });
  }

  return (
    <div style={styles.root}>
      {/* BG pattern */}
      <div style={styles.bgGrid} />
      <div style={styles.bgGlow1} />
      <div style={styles.bgGlow2} />

      {/* HEADER */}
      <header style={styles.header}>
        <div style={styles.logo} onClick={() => setPage("home")}>
          <span style={styles.logoFire}>🔥</span>
          <span style={styles.logoText}>FREE<span style={styles.logoAccent}>FIRE</span></span>
          <span style={styles.logoSub}>TOURNAMENT</span>
        </div>
        <nav style={styles.nav}>
          <button style={{ ...styles.navBtn, ...(page === "home" ? styles.navBtnActive : {}) }} onClick={() => setPage("home")}>🏆 টুর্নামেন্ট</button>
          <button style={{ ...styles.navBtn, ...(page === "create" ? styles.navBtnActive : {}) }} onClick={() => setPage("create")}>➕ তৈরি করুন</button>
        </nav>
      </header>

      {/* HOME PAGE */}
      {page === "home" && (
        <main style={styles.main}>
          <div style={styles.heroSection}>
            <h1 style={styles.heroTitle}>BOOYAH বা বাড়ি যাও!</h1>
            <p style={styles.heroSub}>ফ্রি রেজিস্ট্রেশন • নগদ পুরস্কার • এখনই যোগ দাও</p>
          </div>

          {/* Tabs */}
          <div style={styles.tabs}>
            <button style={{ ...styles.tab, ...(tab === "all" ? styles.tabActive : {}) }} onClick={() => setTab("all")}>সব টুর্নামেন্ট</button>
            <button style={{ ...styles.tab, ...(tab === "joined" ? styles.tabActive : {}) }} onClick={() => setTab("joined")}>আমার টুর্নামেন্ট {joined.length > 0 && <span style={styles.badge}>{joined.length}</span>}</button>
          </div>

          <div style={styles.cardGrid}>
            {filtered.length === 0 && (
              <div style={styles.empty}>এখনো কোনো টুর্নামেন্টে যোগ দেওনি!</div>
            )}
            {filtered.map(t => {
              const isJoined = joined.includes(t.id);
              const pct = Math.round((t.filled / t.slots) * 100);
              return (
                <div key={t.id} style={styles.card}>
                  <div style={styles.cardTop}>
                    <span style={{ ...styles.modeBadge, background: modeColors[t.mode] + "22", color: modeColors[t.mode], border: `1px solid ${modeColors[t.mode]}55` }}>{t.mode}</span>
                    <span style={{ ...styles.statusBadge, ...(t.status === "full" ? styles.statusFull : styles.statusOpen) }}>
                      {t.status === "full" ? "FULL" : "OPEN"}
                    </span>
                  </div>
                  <h2 style={styles.cardName}>{t.name}</h2>
                  <div style={styles.cardMeta}>
                    <span>{mapIcons[t.map]} {t.map}</span>
                    <span>📅 {t.date}</span>
                    <span>⏰ {t.time}</span>
                  </div>
                  <div style={styles.progressWrap}>
                    <div style={{ ...styles.progressBar, width: `${pct}%`, background: pct >= 100 ? "#ff4f4f" : "#00e5ff" }} />
                  </div>
                  <div style={styles.slotText}>{t.filled}/{t.slots} স্লট পূর্ণ</div>
                  <div style={styles.cardBottom}>
                    <div>
                      <div style={styles.prizeLabel}>পুরস্কার</div>
                      <div style={styles.prize}>{t.prize}</div>
                    </div>
                    <div style={{ textAlign: "right" }}>
                      <div style={styles.entryLabel}>এন্ট্রি ফি</div>
                      <div style={styles.entryFree}>{t.entryFee}</div>
                    </div>
                  </div>
                  <button
                    style={{
                      ...styles.joinBtn,
                      ...(isJoined ? styles.joinedBtn : {}),
                      ...(t.status === "full" && !isJoined ? styles.fullBtn : {}),
                    }}
                    onClick={() => !isJoined && t.status !== "full" && handleJoinClick(t)}
                    disabled={isJoined || t.status === "full"}
                  >
                    {isJoined ? "✅ রেজিস্টার্ড" : t.status === "full" ? "স্লট পূর্ণ" : "এখনই যোগ দাও"}
                  </button>
                </div>
              );
            })}
          </div>
        </main>
      )}

      {/* REGISTER PAGE */}
      {page === "register" && selected && (
        <main style={styles.main}>
          <button style={styles.backBtn} onClick={() => setPage("home")}>← ফিরে যাও</button>
          <div style={styles.regCard}>
            <div style={styles.regHeader}>
              <div style={styles.regIcon}>🎮</div>
              <h2 style={styles.regTitle}>{selected.name}</h2>
              <p style={styles.regSub}>{selected.mode} • {selected.map} • {selected.date} • {selected.time}</p>
            </div>

            {!successMsg ? (
              <div style={styles.regForm}>
                <label style={styles.label}>তোমার নাম</label>
                <input style={styles.input} placeholder="যেমন: RaZoR_BD" value={form.name} onChange={e => setForm(f => ({ ...f, name: e.target.value }))} />
                <label style={styles.label}>Free Fire UID</label>
                <input style={styles.input} placeholder="যেমন: 123456789" value={form.uid} onChange={e => setForm(f => ({ ...f, uid: e.target.value }))} maxLength={12} />
                <label style={styles.label}>মোবাইল নম্বর</label>
                <input style={styles.input} placeholder="01XXXXXXXXX" value={form.phone} onChange={e => setForm(f => ({ ...f, phone: e.target.value }))} maxLength={11} />
                {formError && <div style={styles.error}>{formError}</div>}
                <button style={styles.regBtn} onClick={handleRegister}>🔥 রেজিস্ট্রেশন করো</button>
              </div>
            ) : (
              <div style={styles.successBox}>
                <div style={styles.successIcon}>🏆</div>
                <div style={styles.successMsg}>{successMsg}</div>
                <p style={styles.successDetail}>টুর্নামেন্টের আগে রুম আইডি ও পাসওয়ার্ড দেওয়া হবে।</p>
                <button style={styles.regBtn} onClick={() => setPage("home")}>← হোমে ফিরুন</button>
              </div>
            )}
          </div>
        </main>
      )}

      {/* CREATE PAGE */}
      {page === "create" && (
        <main style={styles.main}>
          <button style={styles.backBtn} onClick={() => setPage("home")}>← ফিরে যাও</button>
          <div style={styles.regCard}>
            <div style={styles.regHeader}>
              <div style={styles.regIcon}>⚙️</div>
              <h2 style={styles.regTitle}>নতুন টুর্নামেন্ট তৈরি করো</h2>
            </div>
            <div style={styles.regForm}>
              <label style={styles.label}>টুর্নামেন্টের নাম</label>
              <input style={styles.input} placeholder="যেমন: BEAST CLASH" value={createForm.name} onChange={e => setCreateForm(f => ({ ...f, name: e.target.value }))} />
              <label style={styles.label}>মোড</label>
              <select style={styles.input} value={createForm.mode} onChange={e => setCreateForm(f => ({ ...f, mode: e.target.value }))}>
                <option>Solo</option>
                <option>Duo</option>
                <option>Squad</option>
              </select>
              <label style={styles.label}>ম্যাপ</label>
              <select style={styles.input} value={createForm.map} onChange={e => setCreateForm(f => ({ ...f, map: e.target.value }))}>
                <option>Bermuda</option>
                <option>Kalahari</option>
                <option>Purgatory</option>
              </select>
              <label style={styles.label}>তারিখ</label>
              <input style={styles.input} type="date" value={createForm.date} onChange={e => setCreateForm(f => ({ ...f, date: e.target.value }))} />
              <label style={styles.label}>সময়</label>
              <input style={styles.input} type="time" value={createForm.time} onChange={e => setCreateForm(f => ({ ...f, time: e.target.value }))} />
              <label style={styles.label}>মোট স্লট</label>
              <select style={styles.input} value={createForm.slots} onChange={e => setCreateForm(f => ({ ...f, slots: e.target.value }))}>
                <option value={12}>12</option>
                <option value={16}>16</option>
                <option value={24}>24</option>
                <option value={48}>48</option>
              </select>
              <label style={styles.label}>পুরস্কার (৳)</label>
              <input style={styles.input} placeholder="যেমন: 5000" value={createForm.prize} onChange={e => setCreateForm(f => ({ ...f, prize: e.target.value }))} />
              <button style={styles.regBtn} onClick={handleCreate}>🔥 টুর্নামেন্ট তৈরি করো</button>
            </div>
          </div>
        </main>
      )}

      <footer style={styles.footer}>🔥 Free Fire Tournament App • Made for Champions</footer>
    </div>
  );
}

const styles = {
  root: {
    minHeight: "100vh",
    background: "#080c14",
    color: "#e8eaf0",
    fontFamily: "'Segoe UI', 'Hind Siliguri', sans-serif",
    position: "relative",
    overflowX: "hidden",
  },
  bgGrid: {
    position: "fixed", inset: 0, zIndex: 0,
    backgroundImage: "linear-gradient(rgba(0,229,255,0.04) 1px, transparent 1px), linear-gradient(90deg, rgba(0,229,255,0.04) 1px, transparent 1px)",
    backgroundSize: "40px 40px",
    pointerEvents: "none",
  },
  bgGlow1: {
    position: "fixed", top: "-100px", left: "-100px", width: "400px", height: "400px",
    background: "radial-gradient(circle, rgba(0,229,255,0.08) 0%, transparent 70%)",
    zIndex: 0, pointerEvents: "none",
  },
  bgGlow2: {
    position: "fixed", bottom: "-100px", right: "-80px", width: "350px", height: "350px",
    background: "radial-gradient(circle, rgba(255,79,79,0.07) 0%, transparent 70%)",
    zIndex: 0, pointerEvents: "none",
  },
  header: {
    position: "sticky", top: 0, zIndex: 100,
    background: "rgba(8,12,20,0.92)",
    borderBottom: "1px solid rgba(0,229,255,0.15)",
    backdropFilter: "blur(12px)",
    padding: "0 24px",
    display: "flex", alignItems: "center", justifyContent: "space-between",
    height: "64px",
  },
  logo: {
    display: "flex", alignItems: "center", gap: "8px", cursor: "pointer",
  },
  logoFire: { fontSize: "24px" },
  logoText: {
    fontSize: "20px", fontWeight: 900, letterSpacing: "2px",
    color: "#fff", textTransform: "uppercase",
  },
  logoAccent: { color: "#ff4f4f" },
  logoSub: {
    fontSize: "10px", color: "#00e5ff", letterSpacing: "3px",
    fontWeight: 700, marginLeft: "2px",
  },
  nav: { display: "flex", gap: "8px" },
  navBtn: {
    background: "transparent", border: "1px solid rgba(0,229,255,0.2)",
    color: "#aaa", padding: "8px 16px", borderRadius: "8px",
    cursor: "pointer", fontSize: "13px", fontWeight: 600, transition: "all 0.2s",
  },
  navBtnActive: {
    background: "rgba(0,229,255,0.12)", borderColor: "#00e5ff", color: "#00e5ff",
  },
  main: {
    position: "relative", zIndex: 1,
    maxWidth: "900px", margin: "0 auto", padding: "32px 16px 80px",
  },
  heroSection: {
    textAlign: "center", marginBottom: "32px",
  },
  heroTitle: {
    fontSize: "clamp(28px, 6vw, 48px)", fontWeight: 900, margin: "0 0 8px",
    background: "linear-gradient(90deg, #ff4f4f, #ff9800, #ff4f4f)",
    backgroundClip: "text", WebkitBackgroundClip: "text", color: "transparent",
    letterSpacing: "2px",
  },
  heroSub: {
    color: "#7a8494", fontSize: "14px", letterSpacing: "1px",
  },
  tabs: { display: "flex", gap: "8px", marginBottom: "24px" },
  tab: {
    background: "rgba(255,255,255,0.04)", border: "1px solid rgba(255,255,255,0.08)",
    color: "#7a8494", padding: "10px 20px", borderRadius: "30px",
    cursor: "pointer", fontSize: "14px", fontWeight: 600, transition: "all 0.2s",
    display: "flex", alignItems: "center", gap: "6px",
  },
  tabActive: {
    background: "rgba(0,229,255,0.1)", borderColor: "#00e5ff", color: "#00e5ff",
  },
  badge: {
    background: "#ff4f4f", color: "#fff", borderRadius: "50%",
    width: "18px", height: "18px", display: "inline-flex", alignItems: "center",
    justifyContent: "center", fontSize: "11px",
  },
  cardGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(auto-fill, minmax(270px, 1fr))",
    gap: "20px",
  },
  card: {
    background: "rgba(255,255,255,0.03)",
    border: "1px solid rgba(255,255,255,0.08)",
    borderRadius: "16px", padding: "20px",
    display: "flex", flexDirection: "column", gap: "12px",
    transition: "border-color 0.2s, transform 0.2s",
    cursor: "default",
  },
  cardTop: { display: "flex", justifyContent: "space-between", alignItems: "center" },
  modeBadge: {
    padding: "4px 10px", borderRadius: "20px", fontSize: "11px", fontWeight: 700, letterSpacing: "1px",
  },
  statusBadge: { fontSize: "11px", fontWeight: 700, padding: "4px 10px", borderRadius: "20px" },
  statusOpen: { background: "rgba(0,229,100,0.12)", color: "#00e564", border: "1px solid rgba(0,229,100,0.3)" },
  statusFull: { background: "rgba(255,79,79,0.12)", color: "#ff4f4f", border: "1px solid rgba(255,79,79,0.3)" },
  cardName: { fontSize: "18px", fontWeight: 900, margin: 0, letterSpacing: "1px", color: "#fff" },
  cardMeta: {
    display: "flex", flexWrap: "wrap", gap: "8px",
    fontSize: "12px", color: "#7a8494",
  },
  progressWrap: {
    height: "4px", background: "rgba(255,255,255,0.07)", borderRadius: "2px", overflow: "hidden",
  },
  progressBar: { height: "100%", borderRadius: "2px", transition: "width 0.5s" },
  slotText: { fontSize: "11px", color: "#7a8494" },
  cardBottom: { display: "flex", justifyContent: "space-between", alignItems: "flex-end" },
  prizeLabel: { fontSize: "10px", color: "#7a8494", textTransform: "uppercase", letterSpacing: "1px" },
  prize: { fontSize: "22px", fontWeight: 900, color: "#f5a623" },
  entryLabel: { fontSize: "10px", color: "#7a8494", textTransform: "uppercase", letterSpacing: "1px" },
  entryFree: { fontSize: "16px", fontWeight: 900, color: "#00e564" },
  joinBtn: {
    width: "100%", padding: "12px", borderRadius: "10px",
    background: "linear-gradient(135deg, #ff4f4f, #ff9800)",
    border: "none", color: "#fff", fontSize: "14px", fontWeight: 800,
    cursor: "pointer", letterSpacing: "1px", transition: "opacity 0.2s",
  },
  joinedBtn: {
    background: "rgba(0,229,100,0.12)", color: "#00e564",
    border: "1px solid rgba(0,229,100,0.3)", cursor: "default",
  },
  fullBtn: {
    background: "rgba(255,255,255,0.05)", color: "#555", cursor: "not-allowed",
  },
  empty: { color: "#555", textAlign: "center", padding: "40px 0", fontSize: "16px", gridColumn: "1/-1" },
  backBtn: {
    background: "transparent", border: "1px solid rgba(255,255,255,0.1)",
    color: "#7a8494", padding: "8px 16px", borderRadius: "8px",
    cursor: "pointer", marginBottom: "24px", fontSize: "13px",
  },
  regCard: {
    maxWidth: "480px", margin: "0 auto",
    background: "rgba(255,255,255,0.03)",
    border: "1px solid rgba(0,229,255,0.15)",
    borderRadius: "20px", overflow: "hidden",
  },
  regHeader: {
    background: "linear-gradient(135deg, rgba(255,79,79,0.15), rgba(255,152,0,0.1))",
    padding: "28px 28px 20px", textAlign: "center",
    borderBottom: "1px solid rgba(255,255,255,0.06)",
  },
  regIcon: { fontSize: "40px", marginBottom: "8px" },
  regTitle: { fontSize: "20px", fontWeight: 900, margin: "0 0 4px", color: "#fff" },
  regSub: { fontSize: "12px", color: "#7a8494", margin: 0 },
  regForm: { padding: "24px", display: "flex", flexDirection: "column", gap: "12px" },
  label: { fontSize: "12px", color: "#00e5ff", fontWeight: 700, letterSpacing: "1px", textTransform: "uppercase" },
  input: {
    background: "rgba(255,255,255,0.05)", border: "1px solid rgba(255,255,255,0.1)",
    color: "#fff", padding: "12px 14px", borderRadius: "10px",
    fontSize: "14px", outline: "none", width: "100%", boxSizing: "border-box",
  },
  error: {
    background: "rgba(255,79,79,0.1)", border: "1px solid rgba(255,79,79,0.3)",
    color: "#ff6b6b", borderRadius: "8px", padding: "10px 14px", fontSize: "13px",
  },
  regBtn: {
    width: "100%", padding: "14px", borderRadius: "12px",
    background: "linear-gradient(135deg, #ff4f4f, #ff9800)",
    border: "none", color: "#fff", fontSize: "15px", fontWeight: 800,
    cursor: "pointer", letterSpacing: "1px", marginTop: "4px",
  },
  successBox: {
    padding: "32px 24px", textAlign: "center", display: "flex", flexDirection: "column",
    alignItems: "center", gap: "12px",
  },
  successIcon: { fontSize: "52px" },
  successMsg: { fontSize: "18px", fontWeight: 800, color: "#f5a623" },
  successDetail: { fontSize: "13px", color: "#7a8494", margin: 0 },
  footer: {
    position: "fixed", bottom: 0, left: 0, right: 0, zIndex: 50,
    textAlign: "center", padding: "12px",
    background: "rgba(8,12,20,0.9)", borderTop: "1px solid rgba(255,255,255,0.05)",
    fontSize: "11px", color: "#3a4050", letterSpacing: "1px",
  },
};
