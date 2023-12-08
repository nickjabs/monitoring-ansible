<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Monitoring Setup using Ansible and Terraform</title>
</head>
<body>
<h1>🚀 Monitoring Setup using Ansible and Terraform 🛠️</h1>
<h2>Overview ℹ️</h2>
<p>
  This project demonstrates the orchestration and management of a monitoring infrastructure leveraging Ansible and Terraform. It illustrates the setup and configuration of monitoring tools like Grafana, Prometheus, Alertmanager, and Node Exporter within an AWS environment.
</p>
<h3>Tools Used 🛠️:</h3>
<ul>
  <li><strong>Terraform:</strong> Used for infrastructure provisioning on AWS, managing EC2 instances, VPC settings, and network configurations.</li>
  <li><strong>Ansible:</strong> Orchestrates configuration management and setup for various monitoring services.</li>
</ul>
<h2>Project Structure 📁</h2>
<h3>Terraform (<code>terraform_ec2/</code>)</h3>
<p>
  Manages the infrastructure:
  <ul>
    <li>Creates EC2 instances, defines VPC settings, subnets, security groups, and other necessary resources on AWS.</li>
    <li>Demonstrates the foundational setup required for hosting monitoring services.</li>
  </ul>
</p>
<h3>Ansible (<code>ansible/</code>)</h3>
<p>
  Organizes playbooks and roles for service configurations:
  <ul>
    <li><strong>Playbooks:</strong> Contain specific configurations for each service.</li>
    <li><strong>Roles:</strong> Define tasks and files for individual services, ensuring their setup and configuration according to specified requirements.</li>
  </ul>
</p>
<h4>Playbooks:</h4>
<ul>
  <li><code>alertmanager.yml</code>, <code>grafana.yml</code>, <code>node_exporter.yml</code>, <code>prometheus.yml</code>: Configurations for each service on designated servers.</li>
  <li><code>all.yml</code>: Combined configurations for all services on various servers.</li>
</ul>
<h4>Roles:</h4>
<ul>
  <li><code>alertmanager/</code>, <code>grafana/</code>, <code>node_exporter/</code>, <code>prometheus/</code>: Contain tasks and files for respective service setups.</li>
</ul>
<h2>Usage ⚙️</h2>
<ol>
  <li><strong>Terraform Setup:</strong>
    <ul>
      <li>Navigate to <code>terraform_ec2/</code> and run Terraform commands to provision the infrastructure on AWS.</li>
    </ul>
  </li>
  <li><strong>Ansible Configuration:</strong>
    <ul>
      <li>Ensure Ansible is installed.</li>
      <li>Navigate to <code>ansible/</code> and execute playbooks for desired service configurations.</li>
    </ul>
  </li>
  <li><strong>Execute Monitoring Setup:</strong>
    <ul>
      <li>Run specific playbooks or roles to set up Grafana, Prometheus, Alertmanager, and Node Exporter.</li>
    </ul>
  </li>
  <li><strong>Educational Purposes:</strong>
    <ul>
      <li>Use this project as a learning resource to understand how Terraform and Ansible integrate to deploy and manage a monitoring environment.</li>
      <li>Explore individual playbooks and roles to grasp configurations required for each service.</li>
    </ul>
  </li>
</ol>
<h2>Additional Notes 📝</h2>
<ul>
  <li>The directory structure segregates services, facilitating clear management and orchestration of various monitoring components.</li>
  <li>Each role within Ansible encompasses tasks responsible for configuring and maintaining specific services, ensuring they are operational and running optimally.</li>
</ul>
</body>
</html>