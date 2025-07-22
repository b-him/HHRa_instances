# HHRa_instances
This dataset contains routing instances for a small urban area (~1 km²) located in Hamburg Rahlstedt, 
 intended for multi-modal vehicle routing problems with different transport types.

Each instance varies in the number of customers (from 5 to 200), and consistently includes 2 satellites. For each customer configuration, there are 10 distinct instances. The dataset supports different vehicle types — van (v), bike (b), robot (r), and drone = Euclidean (d) — and provides corresponding distance (in meters) and duration (in seconds) matrices. All distances and durations, except for drone, are computed using the OSRM API based on OpenStreetMap data.
© OpenStreetMap contributors. Data available under the Open Database License (ODbL).

### File Naming Convention

Each file follows the naming structure:

'HHRa_<number_of_customers>\_<number_of_satellites>\_<instance_number>\_<vehicle_type>\_<dist|dur>.csv'

### Instance Structure

Each CSV file is a square matrix of size (n + 3) × (n + 3), where n is the number of customers.

Node 0 is the depot

Nodes 1 to n are customers

The final two nodes (n+1 and n+2) are satellites

Matrix entries represent travel times or distances between nodes for the specified vehicle type and metric.

**Example**:
HHRa_50_2_03_v_dur.csv
→ 50 customers, 2 satellites, instance 3, vehicle type van, duration matrix.
