Load Balancer
This repository contains a simple Python implementation of a Load Balancer. It distributes incoming requests across multiple backend servers to optimize resource use, maximize throughput, minimize response time, and avoid overloading any single server.

Features
Round-robin request distribution

Dynamic server management (add/remove servers)

Basic fault tolerance (handling server failures gracefully)

Requirements
Python 3.7+

No external libraries needed (pure Python)

Usage
Running the Load Balancer
Clone the repository:

bash
Copy
Edit
git clone https://github.com/your-username/load_balancer.git
cd load_balancer
Run the script:

bash
Copy
Edit
python load_balancer.py
Example
You can simulate adding backend servers and sending requests like this:

python
Copy
Edit
lb = LoadBalancer()
lb.add_server("Server 1")
lb.add_server("Server 2")
lb.add_server("Server 3")

print(lb.send_request("Request A"))  # Handled by Server 1
print(lb.send_request("Request B"))  # Handled by Server 2
print(lb.send_request("Request C"))  # Handled by Server 3
print(lb.send_request("Request D"))  # Handled by Server 1 again
Expected Output
arduino
Copy
Edit
Server 1 handling request Request A
Server 2 handling request Request B
Server 3 handling request Request C
Server 1 handling request Request D
Project Structure
kotlin
Copy
Edit
load_balancer.py   # Main Python file with LoadBalancer class
README.md          # Project documentation (this file)
Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.
