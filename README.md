# TripSync – Your Map, Your Way  
*A smarter, faster, and more user-centered navigation tool.*  

## 📖 Overview  
TripSync is a Geographic Information System (GIS) application designed to deliver a customizable and efficient navigation experience. Built with **C++**, **EZGL**, and **GTK**, and powered by the **OpenStreetMap API**, TripSync combines intuitive visuals with state-of-the-art routing algorithms.  

Our vision is to create not just another map, but a **community-driven GIS** where users can crowd-report hazards like potholes or icy roads, making travel safer and more informed.  

---

## 🚀 Key Features  

### 🔎 Visual Elements  
- **Customizable Map Layers** – Toggle subway lines, filter points of interest (POIs), and declutter maps.  
- **POI Filtering** – Quickly find what matters most with user-driven filters.  
- **Subway Line Control** – Empower users with the ability to toggle subway visibility.  
- **Help System** – Popup messages guide users on how to navigate, toggle layers, and use filters.  

Subway Filtering:
<img width="512" height="405" alt="image" src="https://github.com/user-attachments/assets/54cdc8ab-b789-45b6-abd4-4475974eddb2" />

POI Filtering: 
<img width="512" height="405" alt="image" src="https://github.com/user-attachments/assets/d9d2825e-dcf1-4bc0-8272-a455694db88f" />




### 🗺️ Pathfinding Algorithms  
- **A\*** – Optimized pathfinding with travel cost heuristics, achieving an average response time of **0.64 seconds** on complex maps.  
- **Dijkstra’s Algorithm** – Guaranteed shortest path but slower responsiveness.  
- **Breadth-First Search (BFS)** – Provided baseline navigation but returned suboptimal paths.  
- **Optimized Data Structures** – Leveraged **min-heaps** to improve Dijkstra’s efficiency (`O(log N)` vs. `O(N)`).

 <img width="1499" height="942" alt="image" src="https://github.com/user-attachments/assets/dc7aa255-4d65-4280-b0bb-6125fd19fc03" />


### 🚚 Traveling Courier Algorithm  
- **Multi-Destination Dijkstra** – Efficiently preloads data with parallelism (< 5s for large Toronto testcases).  
- **Greedy Initial Solution** – Starts from depots and iteratively finds closest pickups and drop-offs.  
- **2-Opt Heuristic** – Refines delivery routes by systematically exploring better edge swaps.  
- **Simulated Annealing** – Escapes local minima by probabilistically accepting worse solutions, leading to more optimal routes.

  <img width="326" height="422" alt="image" src="https://github.com/user-attachments/assets/cc191026-65c5-4d45-bb30-9ad70e6ec433" />


--- 

## 📊 Metrics & Performance  
- **A\*** average pathfinding response: **0.64s** (Tokyo Map profiling).  
- **Parallel preloading** enables sub-5s setup for large datasets.  
- **2-Opt + Simulated Annealing** reduced courier travel times significantly compared to greedy baselines.  

---

## 🛠️ Technologies Used  
- **C++** – Core implementation language.  
- **EZGL & GTK** – Interactive GUI for map visualization and controls.  
- **OpenStreetMap API** – Base map and real-world road network data.  
- **MongoDB (Planned Extension)** – For hazard reporting and community-driven GIS.  

---

## 🌍 Future Directions  
TripSync aims to become a **crowd-sourced safety GIS**, allowing users to:  
- Report hazards (potholes, black ice, construction, accidents, flooding).  
- Store hazard data in a shared database.  
- Incorporate hazard weights directly into the pathfinding algorithm.  

This transforms TripSync into a **citizen-driven navigation tool** that’s safer and smarter than traditional GIS platforms.  

---

## 👥 Team  
**Team 013**  
- Ved Patel  
- Daunte Figueroa  
- Rayan Ahsan  
