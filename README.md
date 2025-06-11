<html lang="en">
<head>
    <script async src="https://script.adquake.com/js/adquake.js" adquake-key="rrQcJxRTAkGo+Bzpy7P6mg=="></script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ProStory - WhatsApp Story Downloader</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX" crossorigin="anonymous"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        :root {
            --primary: #0d1117;
            --secondary: #161b22;
            --accent: #238636;
            --accent-light: #2ea043;
            --accent-dark: #1c6b2c;
            --text: #e6edf3;
            --text-secondary: #7d8590;
            --card: #161b22;
            --card-border: #30363d;
            --success: #3fb950;
            --error: #f85149;
            --warning: #d29922;
        }

        body {
            background: linear-gradient(135deg, var(--primary), #000);
            color: var(--text);
            min-height: 100vh;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            padding: 30px 0;
            text-align: center;
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid var(--card-border);
        }

        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 10px;
        }

        .logo-icon {
            color: var(--accent-light);
        }

        .logo-text {
            background: linear-gradient(90deg, var(--accent-light), var(--success));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .tagline {
            font-size: 1.1rem;
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto;
        }

        /* Main Content */
        .main-content {
            padding: 50px 0;
        }

        .card {
            background: var(--card);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 40px;
            max-width: 800px;
            margin: 0 auto;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .card-title {
            font-size: 1.8rem;
            text-align: center;
            margin-bottom: 30px;
            color: var(--text);
        }

        .input-group {
            margin-bottom: 25px;
        }

        .input-label {
            display: block;
            margin-bottom: 10px;
            color: var(--text-secondary);
            font-weight: 500;
        }

        .input-container {
            display: flex;
            gap: 15px;
        }

        .url-input {
            flex: 1;
            padding: 16px 24px;
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid var(--card-border);
            border-radius: 8px;
            color: var(--text);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        .url-input:focus {
            outline: none;
            border-color: var(--accent);
            box-shadow: 0 0 0 3px rgba(35, 134, 54, 0.2);
        }

        .paste-btn {
            padding: 0 30px;
            background: linear-gradient(to right, var(--accent), var(--accent-dark));
            border: none;
            border-radius: 8px;
            color: white;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .paste-btn:hover {
            background: linear-gradient(to right, var(--accent-light), var(--accent));
            transform: translateY(-2px);
        }

        .paste-btn:active {
            transform: translateY(0);
        }

        /* Download Section */
        .download-section {
            display: none;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 1px solid var(--card-border);
        }

        .section-title {
            font-size: 1.4rem;
            margin-bottom: 20px;
            color: var(--text);
            text-align: center;
        }

        .quality-options {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .quality-option {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid var(--card-border);
            border-radius: 8px;
            padding: 25px 20px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .quality-option:hover {
            border-color: var(--accent);
            transform: translateY(-5px);
        }

        .quality-option.selected {
            border-color: var(--success);
            background: rgba(35, 134, 54, 0.1);
            box-shadow: 0 5px 15px rgba(35, 134, 54, 0.2);
        }

        .quality-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--accent-light);
        }

        .quality-name {
            font-weight: 600;
            margin-bottom: 5px;
            color: var(--success);
        }

        .quality-desc {
            font-size: 0.9rem;
            color: var(--text-secondary);
        }

        .download-btn-container {
            text-align: center;
            margin-top: 20px;
        }

        .download-btn {
            padding: 16px 50px;
            background: linear-gradient(to right, var(--success), #2c974b);
            border: none;
            border-radius: 8px;
            color: white;
            font-weight: 600;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .download-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(46, 160, 67, 0.3);
        }

        .download-btn:disabled {
            background: var(--text-secondary);
            cursor: not-allowed;
            transform: none;
            box-shadow: none;
        }

        /* Features Section */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 60px 0;
        }

        .feature-card {
            background: var(--card);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 30px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            border-color: var(--accent);
        }

        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--accent-light);
        }

        .feature-title {
            font-size: 1.4rem;
            margin-bottom: 15px;
            color: var(--text);
        }

        .feature-desc {
            color: var(--text-secondary);
            font-size: 1rem;
        }

        /* Ad Container */
        .ad-container {
            background: rgba(22, 27, 34, 0.8);
            border: 1px solid var(--card-border);
            border-radius: 12px;
            padding: 25px;
            text-align: center;
            margin: 50px 0;
        }

        .ad-title {
            font-size: 1.1rem;
            margin-bottom: 15px;
            color: var(--text-secondary);
        }

        .ad-content {
            height: 250px;
            display: flex;
            justify-content: center;
            align-items: center;
            background: rgba(13, 17, 23, 0.5);
            border-radius: 8px;
            color: var(--accent-light);
            font-weight: 500;
            font-size: 1.1rem;
            border: 1px dashed var(--card-border);
        }

        /* Status Message */
        .status-message {
            padding: 20px;
            border-radius: 8px;
            margin-top: 25px;
            text-align: center;
            display: none;
        }

        .status-message.error {
            background: rgba(248, 81, 73, 0.15);
            border: 1px solid var(--error);
            color: var(--error);
        }

        .status-message.success {
            background: rgba(63, 185, 80, 0.15);
            border: 1px solid var(--success);
            color: var(--success);
        }

        /* Footer */
        footer {
            padding: 40px 0 30px;
            border-top: 1px solid var(--card-border);
            margin-top: 40px;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin-bottom: 25px;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--accent-light);
        }

        .copyright {
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .input-container {
                flex-direction: column;
            }
            
            .paste-btn {
                padding: 15px;
                justify-content: center;
            }
            
            .card {
                padding: 30px 20px;
            }
            
            .quality-options {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            .logo {
                font-size: 1.8rem;
            }
            
            .card-title {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="logo">
                <i class="fab fa-whatsapp logo-icon"></i>
                <span class="logo-text">ProStory</span>
            </div>
            <p class="tagline">Download any WhatsApp story in HD quality - Free, Fast & Secure</p>
        </header>

        <main class="main-content">
            <div class="card">
                <h2 class="card-title">Download WhatsApp Stories</h2>
                
                <div class="input-group">
                    <label class="input-label">Paste WhatsApp Story Link:</label>
                    <div class="input-container">
                        <input type="text" class="url-input" id="storyUrl" placeholder="https://wa.story/example123" required>
                        <button class="paste-btn" id="pasteBtn">
                            <i class="fas fa-paste"></i> Paste Link
                        </button>
                    </div>
                </div>
                
                <div class="download-section" id="downloadSection">
                    <h3 class="section-title">Select Download Quality</h3>
                    
                    <div class="quality-options">
                        <div class="quality-option" data-quality="high">
                            <div class="quality-icon">
                                <i class="fas fa-star"></i>
                            </div>
                            <div class="quality-name">High Quality</div>
                            <div class="quality-desc">1080p • 20-30MB</div>
                        </div>
                        
                        <div class="quality-option selected" data-quality="medium">
                            <div class="quality-icon">
                                <i class="fas fa-gem"></i>
                            </div>
                            <div class="quality-name">Medium Quality</div>
                            <div class="quality-desc">720p • 10-15MB</div>
                        </div>
                        
                        <div class="quality-option" data-quality="low">
                            <div class="quality-icon">
                                <i class="fas fa-file-download"></i>
                            </div>
                            <div class="quality-name">Low Quality</div>
                            <div class="quality-desc">480p • 3-5MB</div>
                        </div>
                    </div>
                    
                    <div class="download-btn-container">
                        <button class="download-btn" id="downloadBtn">
                            <i class="fas fa-download"></i> Download Story
                        </button>
                    </div>
                    
                    <div class="status-message" id="statusMessage"></div>
                </div>
            </div>
            
            <div class="ad-container">
                <div class="ad-title">Advertisement</div>
                <div class="ad-content">
                    Ad Space (728 × 250) - AdSense will display here
                </div>
            </div>
            
            <div class="features">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3 class="feature-title">Lightning Fast</h3>
                    <p class="feature-desc">Download stories in seconds with our optimized technology</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-lock"></i>
                    </div>
                    <h3 class="feature-title">100% Secure</h3>
                    <p class="feature-desc">We never store your data or downloaded content</p>
                </div>
                
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-crown"></i>
                    </div>
                    <h3 class="feature-title">Premium Quality</h3>
                    <p class="feature-desc">Download stories in full HD resolution</p>
                </div>
            </div>
            
            <div class="ad-container">
                <div class="ad-title">Advertisement</div>
                <div class="ad-content">
                    Ad Space (300 × 250) - AdSense will display here
                </div>
            </div>
        </main>
        
        <footer>
            <div class="footer-links">
                <a href="#">Privacy Policy</a>
                <a href="#">Terms of Service</a>
                <a href="#">Contact Us</a>
                <a href="#">FAQ</a>
                <a href="#">About</a>
            </div>
            <p class="copyright">© 2023 ProStory - WhatsApp Story Downloader. All rights reserved.</p>
        </footer>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const pasteBtn = document.getElementById('pasteBtn');
            const storyUrlInput = document.getElementById('storyUrl');
            const downloadSection = document.getElementById('downloadSection');
            const qualityOptions = document.querySelectorAll('.quality-option');
            const downloadBtn = document.getElementById('downloadBtn');
            const statusMessage = document.getElementById('statusMessage');
            
            let selectedQuality = 'medium';
            
            // Paste button functionality
            pasteBtn.addEventListener('click', function() {
                navigator.clipboard.readText()
                    .then(text => {
                        if(text.includes('wa.story') || text.includes('whatsapp')) {
                            storyUrlInput.value = text;
                            downloadSection.style.display = 'block';
                            
                            // Scroll to download section
                            downloadSection.scrollIntoView({ behavior: 'smooth', block: 'center' });
                        } else {
                            showStatus('Please copy a valid WhatsApp story link', 'error');
                        }
                    })
                    .catch(err => {
                        console.error('Failed to read clipboard contents: ', err);
                        showStatus('Clipboard access denied. Please paste manually.', 'error');
                    });
            });
            
            // Quality selection
            qualityOptions.forEach(option => {
                option.addEventListener('click', function() {
                    // Remove selected class from all options
                    qualityOptions.forEach(opt => opt.classList.remove('selected'));
                    
                    // Add selected class to clicked option
                    this.classList.add('selected');
                    
                    selectedQuality = this.getAttribute('data-quality');
                });
            });
            
            // Download button functionality
            downloadBtn.addEventListener('click', function() {
                const url = storyUrlInput.value.trim();
                
                if(!url) {
                    showStatus('Please enter a WhatsApp story URL', 'error');
                    return;
                }
                
                // Disable button and show loading
                downloadBtn.disabled = true;
                downloadBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Downloading...';
                statusMessage.style.display = 'none';
                
                // Simulate download process
                setTimeout(() => {
                    // 30% chance of server error
                    const isError = Math.random() < 0.3;
                    
                    if(isError) {
                        // Show server error
                        showStatus('Server error: Unable to download at this time. Please try again later.', 'error');
                    } else {
                        // Show success message
                        showStatus(`Download completed! Your story has been downloaded in ${selectedQuality} quality.`, 'success');
                        
                        // Simulate file download (in a real app, this would start the download)
                        simulateDownload();
                    }
                    
                    // Reset button
                    downloadBtn.disabled = false;
                    downloadBtn.innerHTML = '<i class="fas fa-download"></i> Download Story';
                }, 2500);
            });
            
            // Function to show status messages
            function showStatus(message, type) {
                statusMessage.textContent = message;
                statusMessage.className = 'status-message ' + type;
                statusMessage.style.display = 'block';
                
                // Scroll to message
                statusMessage.scrollIntoView({ behavior: 'smooth', block: 'center' });
            }
            
            // Function to simulate file download
            function simulateDownload() {
                // In a real implementation, this would start the file download
                console.log(`Simulating download: ${storyUrlInput.value} in ${selectedQuality} quality`);
            }
        });
    </script>
</body>
</html>
