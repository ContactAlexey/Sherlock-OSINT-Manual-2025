<h1>OSINT TOOL – SHERLOCK🔍</h1>
<h2>Updated manual for 2025</h2>
<table>
  <tr>
    <td>
      <img src="https://www.kali.org/tools/sherlock/images/sherlock-logo.svg" width="200" alt="sherlocklogo">
    </td>
    <td>
      Sherlock is an OSINT tool designed to search for usernames across hundreds of online platforms. Its goal is to help you check whether an alias exists on social networks, forums, web services, and other sites where a user might have activity.
    </td>
  </tr>
</table>

<p>It is especially useful for:</p>
<ul>
    <li>Professional OSINT investigations</li>
    <li>Digital identity analysis</li>
    <li>Account recovery</li>
    <li>Cybersecurity audits</li>
    <li>Tracking usernames during online investigations</li>
</ul>

<p>Sherlock does NOT hack, nor does it access credentials. It only automates checks to see whether a username is publicly registered on a list of websites.</p>

<hr>

<h2>🔧 BLOCK 1 — Install Sherlock (Old Method, up to 2024)</h2>

<p>This method still works, but it is prone to errors because it depends on the repository and the <em>requirements.txt</em> file, which is no longer used since 2025.</p>

<h3>1. Install Python and Git</h3>
<pre>
sudo apt update
sudo apt install python3 python3-pip git
</pre>

<h3>2. Clone the official repository</h3>
<pre>
git clone https://github.com/sherlock-project/sherlock.git
</pre>

<p>If you get an "RPC failed" error or slow download issues, use shallow cloning:</p>

<pre>
git clone --depth=1 https://github.com/sherlock-project/sherlock.git
</pre>

<h3>3. Enter the project folder</h3>
<pre>
cd sherlock
</pre>

<h3>4. Install dependencies (old method)</h3>
<pre>
pip3 install -r requirements.txt
</pre>

<h3>5. Run Sherlock</h3>
<pre>
python3 sherlock [username]
</pre>

<h3>6. If you cannot clone, download the ZIP</h3>

<p>ZIP page:</p>
<p>https://github.com/sherlock-project/sherlock/archive/refs/heads/master.zip</p>

<p>Extract it:</p>
<pre>
unzip master.zip
cd sherlock-master
</pre>

<p>Install dependencies:</p>
<pre>
pip3 install -r requirements.txt
</pre>

<p>Run:</p>
<pre>
python3 sherlock.py [username]
</pre>

<p><strong>⚠️ This method became obsolete in 2025 because Sherlock no longer uses requirements.txt.</strong></p>

<hr>

<h2>🔧 BLOCK 2 — Modern Installation 2025 (RECOMMENDED)</h2>

<p>Since 2025, Sherlock is distributed as an official Python package managed with <strong>pipx</strong>.</p>

<h3>1. Check Python 3 + pip</h3>
<pre>
sudo apt update
sudo apt install python3 python3-pip -y
</pre>

<h3>2. Install pipx (if you don’t have it)</h3>
<pre>
sudo apt install pipx
pipx ensurepath
</pre>

<h3>3. Install Sherlock with pipx</h3>
<pre>
pipx install sherlock-project
</pre>

<p>This method:</p>
<ul>
    <li>Does not require cloning repositories</li>
    <li>Installs all dependencies automatically</li>
    <li>Allows running Sherlock from any directory</li>
</ul>

<h3>4. Run Sherlock</h3>
<pre>
sherlock [username]
</pre>

<p>You no longer need to run <code>python3 sherlock.py</code>.</p>

<hr>

<h2>⚙️ BLOCK 3 — Basic Usage</h2>

<p>Search for a username:</p>
<pre>
sherlock [username]
</pre>

<p>Save results to a file:</p>
<pre>
sherlock [username] --output results.txt
</pre>

<p>Save results in JSON:</p>
<pre>
sherlock [username] --json
</pre>

<p>Increase speed:</p>
<pre>
sherlock [username] --timeout 5 --threads 20
</pre>

<p><strong>⚠️ Warning:</strong> using too many threads may cause blocks or false positives.</p>

<hr>

<h2>💡 BLOCK 4 — Practical Tips</h2>

<ul>
    <li>If you get many timeouts, reduce the threads.</li>
    <li>When doing real OSINT work, avoid aggressive VPNs — some sites block requests.</li>
    <li>Do not investigate real usernames without permission.</li>
</ul>

<h2>Official Information</h2>

<p>Kali Linux page:</p>
<p>https://www.kali.org/tools/sherlock/</p>

<p>Repository:</p>
<p>https://github.com/sherlock-project/sherlock</p>
