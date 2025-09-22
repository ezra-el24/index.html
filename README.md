<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2005 Girly Calendar</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Satisfy&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --light-pink: #fde8f2;
            --medium-pink: #f7a2d4;
            --dark-pink: #e37abf;
            --dark-text: #4a4a4a;
            --white-text: #ffffff;
            --border-color: #f0e1e9;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            color: var(--dark-text);
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 2rem;
            min-height: 100vh;
            
            background-color: var(--light-pink);
            background-image: radial-gradient(var(--medium-pink) 1px, transparent 1px), radial-gradient(var(--medium-pink) 1px, var(--light-pink) 1px);
            background-size: 20px 20px;
            background-position: 0 0, 10px 10px;
        }

        .calendar-container {
            width: 100%;
            max-width: 1200px;
            background-color: #fff;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
            border: 5px solid var(--medium-pink);
        }

        .header {
            text-align: center;
            font-family: 'Satisfy', cursive;
            font-size: 5rem;
            color: var(--dark-pink);
            margin-bottom: 2rem;
            position: relative;
            padding-top: 20px;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.1);
        }

        .bow-left, .bow-right {
            position: absolute;
            top: 0;
            font-size: 8rem;
            line-height: 1;
            color: var(--medium-pink);
            text-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 10;
        }

        .bow-left {
            left: 0;
            transform: scaleX(-1) rotate(15deg);
        }
        
        .bow-right {
            right: 0;
            transform: rotate(-15deg);
        }
        
        .months-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .month-card {
            background-color: #fff;
            border-radius: 12px;
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
            border: 2px solid var(--border-color);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .month-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.12);
        }

        .month-title {
            font-family: 'Satisfy', cursive;
            font-size: 2.5rem;
            color: var(--dark-pink);
            margin-top: 0;
            margin-bottom: 1rem;
        }

        .days-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 5px;
        }

        .day-header {
            font-weight: bold;
            text-transform: uppercase;
            font-size: 0.9rem;
            color: var(--dark-text);
        }
        
        .day-cell {
            padding: 0.5rem;
            text-align: center;
            border-radius: 6px;
            background-color: var(--light-pink);
            position: relative;
            overflow: hidden;
            border: 1px solid var(--border-color);
            transition: transform 0.2s ease-in-out;
        }

        .day-cell:hover:not(.empty-day) {
            transform: scale(1.05);
            background-color: var(--medium-pink);
            color: var(--white-text);
        }

        .empty-day {
            background-color: transparent;
            border: 1px solid transparent;
        }

        .holiday {
            color: var(--white-text);
            cursor: pointer;
            font-weight: bold;
        }
        
        .ph-holiday {
            background-color: #d354a5;
        }
        
        .birthday {
            background-color: #ff69b4;
        }

        .ph-holiday:hover { background-color: #b33989; }
        .birthday:hover { background-color: #ff1493; }

        .holiday-note {
            position: absolute;
            bottom: 2px;
            right: 2px;
            font-size: 0.6rem;
            color: var(--white-text);
            padding: 2px 4px;
            border-radius: 4px;
            background-color: rgba(0, 0, 0, 0.2);
            line-height: 1;
        }
        
        .holiday-notes-container {
            position: absolute;
            bottom: 2px;
            right: 2px;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
            gap: 2px;
        }

        @media (max-width: 768px) {
            .header {
                font-size: 3rem;
            }
            .months-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <div class="calendar-container">
        <h1 class="header">
            <div class="bow-left">
                ౨ৎ
            </div>
            2005
            <div class="bow-right">
                ౨ৎ
            </div>
        </h1>

        <div class="months-grid">
            <div class="month-card">
                <h2 class="month-title">January</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell holiday ph-holiday" title="New Year's Day">
                        1
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell holiday ph-holiday" title="Eid al-Adha">
                        21
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                    <div class="day-cell">31</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">February</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell holiday ph-holiday" title="People Power Anniversary">
                        25
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">March</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell holiday ph-holiday" title="Maundy Thursday">
                        24
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell holiday ph-holiday" title="Good Friday">
                        25
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell holiday ph-holiday" title="Black Saturday">
                        26
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                    <div class="day-cell">31</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">April</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell holiday ph-holiday" title="The Day of Valor">
                        9
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">May</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell holiday ph-holiday" title="Labor Day">
                        1
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                    <div class="day-cell">31</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">June</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell holiday ph-holiday" title="Independence Day">
                        12
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">July</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell holiday ph-holiday" title="Special Non-working Day (Metro Manila)">
                        25
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                    <div class="day-cell">31</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">August</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell holiday ph-holiday" title="Ninoy Aquino Day">
                        21
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell holiday ph-holiday" title="National Heroes Day">
                        29
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">30</div>
                    <div class="day-cell">31</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">September</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">October</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell">30</div>
                    <div class="day-cell">31</div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">November</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell holiday birthday" title="Jez Born Day">
                        24
                        <div class="holiday-notes-container"><span class="holiday-note">B-Day</span></div>
                    </div>
                    <div class="day-cell">25</div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell holiday ph-holiday" title="Special Non-working Holiday">
                        28
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">29</div>
                    <div class="day-cell holiday ph-holiday" title="Bonifacio Day">
                        30
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                </div>
            </div>

            <div class="month-card">
                <h2 class="month-title">December</h2>
                <div class="days-grid">
                    <div class="day-header">S</div>
                    <div class="day-header">M</div>
                    <div class="day-header">T</div>
                    <div class="day-header">W</div>
                    <div class="day-header">T</div>
                    <div class="day-header">F</div>
                    <div class="day-header">S</div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell empty-day"></div>
                    <div class="day-cell">1</div>
                    <div class="day-cell">2</div>
                    <div class="day-cell">3</div>
                    <div class="day-cell">4</div>
                    <div class="day-cell">5</div>
                    <div class="day-cell">6</div>
                    <div class="day-cell">7</div>
                    <div class="day-cell">8</div>
                    <div class="day-cell">9</div>
                    <div class="day-cell">10</div>
                    <div class="day-cell">11</div>
                    <div class="day-cell">12</div>
                    <div class="day-cell">13</div>
                    <div class="day-cell">14</div>
                    <div class="day-cell">15</div>
                    <div class="day-cell">16</div>
                    <div class="day-cell">17</div>
                    <div class="day-cell">18</div>
                    <div class="day-cell">19</div>
                    <div class="day-cell">20</div>
                    <div class="day-cell">21</div>
                    <div class="day-cell">22</div>
                    <div class="day-cell">23</div>
                    <div class="day-cell">24</div>
                    <div class="day-cell holiday ph-holiday" title="Christmas Day">
                        25
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell">26</div>
                    <div class="day-cell">27</div>
                    <div class="day-cell">28</div>
                    <div class="day-cell">29</div>
                    <div class="day-cell holiday ph-holiday" title="Rizal Day">
                        30
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                    <div class="day-cell holiday ph-holiday" title="New Year's Eve">
                        31
                        <div class="holiday-notes-container"><span class="holiday-note">PH</span></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
