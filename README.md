# Shadow
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Video Download - Jade Dynasty S03E20-26</title>
    <meta name="description" content="Download high quality video episodes">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
  background: url("Madness/images.jpg") no-repeat center center fixed; /* آدرس تصویر */   
  background-size: cover; /* تصویر رو تمام صفحه می‌کشه */
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  position: relative;
  overflow: hidden;
}
        }

        /* Animated particle background */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 0;
        }

        .particle {
            position: absolute;
            width: 2px;
            height: 2px;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            animation: float 20s infinite;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0) translateX(0);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) translateX(50px);
                opacity: 0;
            }
        }

        .container {
            position: relative;
            z-index: 1;
            width: 90%;
            max-width: 380px;
            margin: 0 auto;
        }

        .video-card {
            background: rgba(30, 41, 59, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 24px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .video-wrapper {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%; /* 1:1 aspect ratio - square */
            background: #000;
            border-radius: 12px;
            overflow: hidden;
            margin-bottom: 20px;
        }

        video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 16px;
        }

        .video-title {
            font-size: 22px;
            font-weight: 700;
            color: #60a5fa;
            margin-bottom: 6px;
            line-height: 1.3;
        }

        .video-subtitle {
            font-size: 14px;
            color: rgba(255, 255, 255, 0.6);
            margin-bottom: 18px;
        }

        .download-section {
            display: flex;
            gap: 12px;
            align-items: center;
            flex-wrap: wrap;
        }

        .quality-selector {
            position: relative;
            flex: 0 0 auto;
        }

        .quality-button {
            background: rgba(15, 23, 42, 0.8);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: #fff;
            padding: 10px 18px;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s ease;
            min-width: 110px;
            justify-content: space-between;
        }

        .quality-button:hover {
            background: rgba(15, 23, 42, 1);
            border-color: rgba(255, 255, 255, 0.3);
        }

        .quality-button::after {
            content: '▼';
            font-size: 12px;
            transition: transform 0.3s ease;
        }

        .quality-button.active::after {
            transform: rotate(180deg);
        }

        .quality-dropdown {
            position: absolute;
            top: calc(100% + 8px);
            left: 0;
            right: 0;
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 12px;
            overflow: hidden;
            display: none;
            z-index: 10;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
        }

        .quality-dropdown.active {
            display: block;
            animation: slideDown 0.3s ease;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .quality-option {
            padding: 10px 16px;
            cursor: pointer;
            transition: background 0.2s ease;
            color: #fff;
            font-size: 14px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .quality-option:hover {
            background: rgba(96, 165, 250, 0.2);
        }

        .quality-option.selected {
            background: rgba(96, 165, 250, 0.3);
        }

        .quality-option::after {
            content: '○';
            font-size: 20px;
            color: rgba(255, 255, 255, 0.3);
        }

        .quality-option.selected::after {
            content: '◉';
            color: #60a5fa;
        }

        .download-button {
            background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
            border: none;
            color: #fff;
            padding: 10px 24px;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            flex: 1;
            justify-content: center;
            box-shadow: 0 4px 20px rgba(59, 130, 246, 0.3);
            min-width: 130px;
        }

        .download-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 30px rgba(59, 130, 246, 0.5);
        }

        .download-button:active {
            transform: translateY(0);
        }

        .download-icon {
            font-size: 16px;
        }

        /* Mobile responsiveness */
        @media (max-width: 640px) {
            .video-card {
                padding: 20px;
                border-radius: 16px;
            }

            .video-title {
                font-size: 22px;
            }

            .video-subtitle {
                font-size: 14px;
            }

            .download-section {
                flex-direction: column;
                width: 100%;
            }

            .quality-selector {
                width: 100%;
            }

            .quality-button {
                width: 100%;
            }

            .download-button {
                width: 100%;
            }
        }

        @media (max-width: 480px) {
            body {
                padding: 12px;
            }

            .video-card {
                padding: 16px;
            }

            .video-title {
                font-size: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Particle background -->
    <div class="particles" id="particles"></div>

    <div class="container">
        <div class="video-card">
            <!-- Video Player -->
            <div class="video-wrapper">
                <video id="videoPlayer" controls controlsList="nodownload">
                    <source src="videos/Animo.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
            </div>

            <!-- Video Info -->
            <h1 class="video-title">انیمو</h1>
            <p class="video-subtitle">انیمو هنتای تقدیم میکند </p>

            <!-- Download Section -->
            <div class="download-section">
                <!-- Quality Selector -->
                <div class="quality-selector">
                    <button class="quality-button" id="qualityButton">
                        <span id="selectedQuality">کیفیت خودکار</span>
                    </button>
                    <div class="quality-dropdown" id="qualityDropdown">
                        <div class="quality-option" data-quality="480p" data-url="videos/VideoTest1.mp4">480p</div>
                        <div class="quality-option" data-quality="720p" data-url="M.mp4">720p</div>
                        <div class="quality-option" data-quality="1080p" data-url="YOUR_1080P_VIDEO_URL.mp4">1080p</div>
                    </div>
                </div>

                <!-- Download Button -->
                <button class="download-button" id="downloadButton">
                    <span class="download-icon">⬇</span>
                    <span>دانلود</span>
                </button>
            </div>
        </div>
    </div>

    <script>
        // Create animated particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;

            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 20 + 's';
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                particlesContainer.appendChild(particle);
            }
        }

        createParticles();

        // Quality selector functionality
        const qualityButton = document.getElementById('qualityButton');
        const qualityDropdown = document.getElementById('qualityDropdown');
        const qualityOptions = document.querySelectorAll('.quality-option');
        const selectedQualityText = document.getElementById('selectedQuality');
        const videoPlayer = document.getElementById('videoPlayer');
        let currentVideoUrl = 'YOUR_2160P_VIDEO_URL.mp4';

        // Toggle dropdown
        qualityButton.addEventListener('click', (e) => {
            e.stopPropagation();
            qualityDropdown.classList.toggle('active');
            qualityButton.classList.toggle('active');
        });

        // Close dropdown when clicking outside
        document.addEventListener('click', () => {
            qualityDropdown.classList.remove('active');
            qualityButton.classList.remove('active');
        });

        // Select quality
        qualityOptions.forEach(option => {
            option.addEventListener('click', (e) => {
                e.stopPropagation();
                
                // Remove selected class from all options
                qualityOptions.forEach(opt => opt.classList.remove('selected'));
                
                // Add selected class to clicked option
                option.classList.add('selected');
                
                // Update selected quality text
                const quality = option.dataset.quality;
                selectedQualityText.textContent = quality;
                
                // Update video source
                currentVideoUrl = option.dataset.url;
                const currentTime = videoPlayer.currentTime;
                videoPlayer.src = currentVideoUrl;
                videoPlayer.currentTime = currentTime;
                
                // Close dropdown
                qualityDropdown.classList.remove('active');
                qualityButton.classList.remove('active');
            });
        });

        // Download button functionality
        const downloadButton = document.getElementById('downloadButton');
        downloadButton.addEventListener('click', () => {
            const link = document.createElement('a');
            link.href = currentVideoUrl;
            link.download = 'video_' + selectedQualityText.textContent + '.mp4';
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
        });

        // Prevent right-click on video (optional protection)
        videoPlayer.addEventListener('contextmenu', (e) => {
            e.preventDefault();
        });
    </script>
</body>
</html>
