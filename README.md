<h1>🚀 Smart Application Performance Monitoring and Auto-Scaling System</h1>

  <p>A real-time intelligent system that monitors synthetic application performance metrics, predicts incoming traffic, detects anomalies, and auto-scales AWS EC2 instances based on forecasted demand.</p>

  <hr>

  <h2>📊 Problem Statement</h2>
  <p><strong>Objective:</strong> Build a system that monitors application performance metrics and automatically scales resources based on predicted demand.</p>
  <ul>
    <li>AI/ML-driven demand forecasting (LSTM)</li>
    <li>Real-time anomaly detection</li>
    <li>Auto-scaling of EC2 instances via AWS SDK (boto3)</li>
    <li>Modular system design with cloud integration</li>
  </ul>

  <h2>🌐 Architecture Overview</h2>
  <pre>
[Data Simulation] → [Preprocessing] → [LSTM Forecasting Model] → [Anomaly Detection]
     → [Decision Engine] → [AWS EC2 AutoScaler] → [Scaling Action]
  </pre>

  <h2>💻 Tech Stack</h2>
  <ul>
    <li><strong>Data:</strong> Synthetic traffic using NumPy</li>
    <li><strong>Model:</strong> LSTM using Keras/TensorFlow</li>
    <li><strong>API:</strong> AWS EC2 via boto3</li>
    
  </ul>

  <h2>📊 Features Implemented</h2>
  <ul>
    <li>✅ Real-time traffic prediction</li>
    <li>✅ Anomaly detection logic</li>
    <li>✅ Auto-scaling using EC2 and boto3</li>
    <li>✅ Live simulation loop (1-min interval)</li>
  </ul>

  <h2>📂 Dataset</h2>
  <p>Simulated 200,000-minute time series traffic with daily patterns, noise, and spikes.</p>

  <h2>🔧 How to Run</h2>
  <ol>
    <li>Clone this repository or open in Google Colab.</li>
    <li>Install dependencies:<br>
      <code>pip install boto3 schedule tensorflow pandas matplotlib</code></li>
    <li>Set AWS credentials at the top of the notebook:
      <pre><code>
import os
os.environ['AWS_ACCESS_KEY_ID'] = 'your-access-key'
os.environ['AWS_SECRET_ACCESS_KEY'] = 'your-secret-key'
os.environ['AWS_DEFAULT_REGION'] = 'us-east-1'
      </code></pre>
    </li>
    <li>Ensure EC2 instances have the tag:
      <ul>
        <li>Key: <code>AutoScaleGroup</code></li>
        <li>Value: <code>SmartScaler</code></li>
      </ul>
    </li>
    <li>Run all cells to start the real-time auto-scaling loop.</li>
  </ol>

  <h2>🏠 AWS Setup</h2>
  <ul>
    <li>Region: <code>us-east-1</code></li>
    <li>IAM Permissions required:
      <ul>
        <li>ec2:StartInstances</li>
        <li>ec2:StopInstances</li>
        <li>ec2:DescribeInstances</li>
      </ul>
    </li>
    <li>Ensure at least 1 EC2 instance is in a <strong>stopped</strong> state for scaling up.</li>
  </ul>

  <h2>📡 Output Example</h2>
  <pre>
[Scaler] Target: 2, Running: 1, Stopped: 1
[EC2] Starting instance i-0abc123...
[2025-07-07 12:01:22] Predicted Req: 345.1, Anomaly: True, Nodes: 2
  </pre>

  <h2>🎯 Skills Demonstrated</h2>
  <ul>
    <li><strong>AI/ML:</strong> LSTM time series forecasting</li>
    <li><strong>DevOps:</strong> Cloud infrastructure scaling with boto3</li>
    <li><strong>System Design:</strong> Modular, real-time reactive system</li>
  </ul>

  <h2>🌟 Improvements</h2>
  <ul>
    <li>Use real APM logs (e.g., Prometheus, Datadog)</li>
    <li>Add dashboard (Streamlit, Grafana)</li>
    <li>Move credentials to AWS Secrets Manager or IAM roles</li>
  </ul>


  <h2>📁 Project Structure</h2>
  <pre>
smart-autoscaler/
├── smart_autoscaler.ipynb     # Notebook with model + boto3
├── requirements.txt           # Dependencies
├── README.md                  # Markdown version
├── README.html                # This file
  </pre>

 
