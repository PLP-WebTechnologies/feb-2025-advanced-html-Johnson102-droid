<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Advanced HTML5 assignment for Web Development course">
    <title>Advanced HTML5 - Web Development</title>
    <style>
        :root {
            --primary: #3a86ff;
            --secondary: #8338ec;
            --accent: #ff006e;
            --dark: #1a1a2e;
            --light: #f8f9fa;
        }
        
        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            line-height: 1.6;
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            background-color: var(--light);
            color: var(--dark);
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem;
            border-radius: 0.5rem;
            margin-bottom: 2rem;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        h1, h2, h3 {
            color: var(--dark);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }
        
        section {
            background: white;
            padding: 1.5rem;
            border-radius: 0.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }
        
        ol.roman {
            list-style-type: upper-roman;
            padding-left: 2rem;
        }
        
        ol.roman li {
            margin-bottom: 0.5rem;
            position: relative;
            left: 1rem;
        }
        
        figure {
            margin: 0;
            text-align: center;
        }
        
        img {
            max-width: 100%;
            height: auto;
            border-radius: 0.5rem;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
        
        img:hover {
            transform: scale(1.02);
        }
        
        figcaption {
            margin-top: 0.5rem;
            font-style: italic;
            color: #666;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1.5rem 0;
            box-shadow: 0 2px 3px rgba(0,0,0,0.1);
        }
        
        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        
        th {
            background-color: var(--primary);
            color: white;
            font-weight: 600;
        }
        
        tr:nth-child(even) {
            background-color: #f8f9fa;
        }
        
        tr:hover {
            background-color: #e9ecef;
        }
        
        form {
            background: white;
            padding: 1.5rem;
            border-radius: 0.5rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }
        
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        .form-group {
            margin-bottom: 1rem;
        }
        
        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--dark);
        }
        
        .required label::after {
            content: " *";
            color: var(--accent);
        }
        
        input, select, textarea {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #ddd;
            border-radius: 0.25rem;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s, box-shadow 0.3s;
        }
        
        input:focus, select:focus, textarea:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(58, 134, 255, 0.2);
        }
        
        input[type="color"] {
            height: 3rem;
            padding: 0.25rem;
            cursor: pointer;
        }
        
        input[type="range"] {
            -webkit-appearance: none;
            height: 0.5rem;
            background: #ddd;
            border-radius: 0.25rem;
            padding: 0;
        }
        
        input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 1.25rem;
            height: 1.25rem;
            background: var(--primary);
            border-radius: 50%;
            cursor: pointer;
        }
        
        .range-value {
            display: inline-block;
            min-width: 2rem;
            text-align: center;
            font-weight: 600;
            color: var(--primary);
        }
        
        button {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 0.75rem 1.5rem;
            border: none;
            border-radius: 0.25rem;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .multimedia-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        video, audio {
            width: 100%;
            border-radius: 0.5rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        @media (max-width: 768px) {
            .multimedia-container {
                grid-template-columns: 1fr;
            }
            
            .form-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Advanced HTML5 Elements</h1>
        <p>Web Development Course Assignment</p>
    </header>
    
    <main>
        <section aria-labelledby="ordered-list-heading">
            <h2 id="ordered-list-heading">Ordered List with Roman Numerals</h2>
            <ol class="roman">
                <li>HTML5 Semantic Elements</li>
                <li>Advanced Form Controls</li>
                <li>Multimedia Integration</li>
                <li>CSS3 Styling Techniques</li>
                <li>Responsive Design Principles</li>
            </ol>
        </section>
        
        <section aria-labelledby="image-heading">
            <h2 id="image-heading">Technology Image from Pexels</h2>
            <figure>
                <img src="https://images.pexels.com/photos/577585/pexels-photo-577585.jpeg" 
                     alt="Computer screen displaying colorful programming code" 
                     width="800"
                     height="450">
                <figcaption>Modern web development environment with code editor</figcaption>
            </figure>
        </section>
        
        <section aria-labelledby="contacts-heading">
            <h2 id="contacts-heading">Developer Contacts Table</h2>
            <table>
                <thead>
                    <tr>
                        <th scope="col">Name</th>
                        <th scope="col">Address</th>
                        <th scope="col">Mobile</th>
                        <th scope="col">Email</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>James Wachira</td>
                        <td>123 Tech Hub, Nairobi</td>
                        <td>+254 712 345 678</td>
                        <td><a href="mailto:james.wachira@gmail.com">james.wachira@gmail.com</a></td>
                    </tr>
                    <tr>
                        <td>Ben Kipyegon</td>
                        <td>456 Developer Plaza, Mombasa</td>
                        <td>+254 723 456 789</td>
                        <td><a href="mailto:ben.kipyegon@gmail.com">ben.kipyegon@gmail.com</a></td>
                    </tr>
                    <tr>
                        <td>Elijah Sila</td>
                        <td>789 Code Street, Kisumu</td>
                        <td>+254 734 567 890</td>
                        <td><a href="mailto:elijah.sila@gmail.com">elijah.sila@gmail.com</a></td>
                    </tr>
                    <tr>
                        <td>Kennedy Kamau</td>
                        <td>321 Web Avenue, Nakuru</td>
                        <td>+254 745 678 901</td>
                        <td><a href="mailto:kennedy.kamau@gmail.com">kennedy.kamau@gmail.com</a></td>
                    </tr>
                    <tr>
                        <td>Simon Mwaura</td>
                        <td>654 Digital Lane, Eldoret</td>
                        <td>+254 756 789 012</td>
                        <td><a href="mailto:simon.mwaura@gmail.com">simon.mwaura@gmail.com</a></td>
                    </tr>
                </tbody>
            </table>
        </section>
        
        <section aria-labelledby="form-heading">
            <h2 id="form-heading">Advanced Developer Registration</h2>
            <form id="developerForm" novalidate>
                <div class="form-grid">
                    <div class="form-group required">
                        <label for="fullName">Full Name</label>
                        <input type="text" id="fullName" name="fullName" required 
                               minlength="3" maxlength="50"
                               placeholder="Enter your full name"
                               pattern="[A-Za-z ]+"
                               title="Only letters and spaces allowed">
                    </div>
                    
                    <div class="form-group required">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" name="email" required
                               placeholder="your.email@gmail.com">
                    </div>
                    
                    <div class="form-group">
                        <label for="phone">Phone Number</label>
                        <input type="tel" id="phone" name="phone"
                               pattern="[\+]\d{3} \d{3} \d{3} \d{3}"
                               placeholder="+254 123 456 789">
                    </div>
                    
                    <div class="form-group">
                        <label for="birthdate">Date of Birth</label>
                        <input type="date" id="birthdate" name="birthdate">
                    </div>
                    
                    <div class="form-group">
                        <label for="website">Portfolio Website</label>
                        <input type="url" id="website" name="website"
                               placeholder="https://yourportfolio.com">
                    </div>
                    
                    <div class="form-group">
                        <label for="favColor">Favorite Color</label>
                        <input type="color" id="favColor" name="favColor" value="#3a86ff">
                    </div>
                    
                    <div class="form-group">
                        <label for="experience">Experience Level <span class="range-value">5</span>/10</label>
                        <input type="range" id="experience" name="experience" 
                               min="0" max="10" step="1" value="5">
                    </div>
                    
                    <div class="form-group">
                        <label for="specialty">Development Specialty</label>
                        <select id="specialty" name="specialty">
                            <option value="">Select your specialty</option>
                            <option value="frontend">Frontend Development</option>
                            <option value="backend">Backend Development</option>
                            <option value="fullstack">Full Stack Development</option>
                            <option value="mobile">Mobile Development</option>
                            <option value="devops">DevOps Engineering</option>
                        </select>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="bio">Developer Bio</label>
                    <textarea id="bio" name="bio" rows="5"
                              placeholder="Tell us about your skills and experience..."></textarea>
                </div>
                
                <div class="form-group">
                    <label for="newsletter">
                        <input type="checkbox" id="newsletter" name="newsletter" checked>
                        Subscribe to developer newsletter
                    </label>
                </div>
                
                <div class="form-group">
                    <label for="terms">
                        <input type="checkbox" id="terms" name="terms" required>
                        I agree to the terms and conditions
                    </label>
                </div>
                
                <button type="submit">Register as Developer</button>
            </form>
        </section>
        
        <section aria-labelledby="multimedia-heading">
            <h2 id="multimedia-heading">Technology Multimedia</h2>
            <div class="multimedia-container">
                <div>
                    <h3>Web Development Video</h3>
                    <video width="800" height="450" controls poster="https://images.pexels.com/photos/270632/pexels-photo-270632.jpeg">
                        <source src="https://samplelib.com/lib/preview/mp4/sample-5s.mp4" type="video/mp4">
                        Your browser does not support HTML5 video. Here's a <a href="https://samplelib.com/lib/preview/mp4/sample-5s.mp4">link to the video</a> instead.
                    </video>
                </div>
                
                <div>
                    <h3>Tech Podcast</h3>
                    <audio controls>
                        <source src="https://samplelib.com/lib/preview/mp3/sample-3s.mp3" type="audio/mpeg">
                        Your browser does not support the audio element. Here's a <a href="https://samplelib.com/lib/preview/mp3/sample-3s.mp3">link to the audio</a> instead.
                    </audio>
                </div>
            </div>
        </section>
    </main>
    
    <script>
        // Form validation and interaction
        document.getElementById('developerForm').addEventListener('submit', function(e) {
            if (!this.checkValidity()) {
                e.preventDefault();
                alert('Please fill out all required fields correctly.');
            } else {
                alert('Form submitted successfully! (This is a demo)');
            }
        });

        // Update range value display
        const experienceSlider = document.getElementById('experience');
        const rangeValue = document.querySelector('.range-value');
        
        experienceSlider.addEventListener('input', function() {
            rangeValue.textContent = this.value;
        });

        // Add focus styles for keyboard navigation
        document.addEventListener('keyup', function(e) {
            if (e.key === 'Tab') {
                const focusedElement = document.activeElement;
                if (focusedElement.matches('input, select, textarea, button')) {
                    focusedElement.style.boxShadow = '0 0 0 3px rgba(255, 0, 110, 0.3)';
                    
                    // Remove shadow when focus is lost
                    focusedElement.addEventListener('blur', function() {
                        this.style.boxShadow = '';
                    }, { once: true });
                }
            }
        });
    </script>
</body>
</html>
            <div class="form-group">
                <label for="experience">Tech Experience Level</label>
                <input type="range" id="experience" name="experience" 
                       min="0" max="10" value="5">
                <span id="expValue">5</span>/10
            </div>
            
            <div class="form-group">
                <label for="message">Why interested in technology?</label>
                <textarea id="message" name="message" rows="4"
                          placeholder="Tell us about your tech interests..."></textarea>
            </div>
            
            <div class="form-group">
                <label for="subscribe">
                    <input type="checkbox" id="subscribe" name="subscribe" checked>
                    Subscribe to tech newsletter
                </label>
            </div>
            
            <button type="submit">Register Now</button>
        </form>
    </section>
    
    <section class="multimedia">
        <h2>Technology Multimedia</h2>
        
        <div>
            <h3>Tech Video</h3>
            <video width="800" controls>
                <source src="https://samplelib.com/lib/preview/mp4/sample-5s.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
        
        <div>
            <h3>Tech Podcast</h3>
            <audio controls>
                <source src="https://samplelib.com/lib/preview/mp3/sample-3s.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
        </div>
    </section>
    
    <script>
        document.getElementById('techForm').addEventListener('submit', function(e) {
            if (!this.checkValidity()) {
                e.preventDefault();
                alert('Please fill out all required fields correctly.');
            }
        });

        // Show experience level value
        const experienceSlider = document.getElementById('experience');
        const expValue = document.getElementById('expValue');
        experienceSlider.addEventListener('input', function() {
            expValue.textContent = this.value;
        });
    </script>
</body>
</html>
