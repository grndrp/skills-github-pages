<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Green Drop Membership Comparison</title>
    <style>
        body {
            font-family: Georgia, serif;
            margin: 0;
            padding: 0;
            background: #fafafa;
            color: #333;
        }
        
        .green-drop-container {
            font-family: Georgia, serif;
            margin: 0;
            padding: 20px;
            background: #fafafa;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .green-drop-header {
            background: linear-gradient(135deg, #6151a2 0%, #9fcc3b 100%);
            color: white;
            padding: 2rem;
            text-align: center;
        }
        
        .green-drop-header h1 {
            font-family: Arial, sans-serif;
            font-size: 3rem;
            font-weight: bold;
            margin: 0 0 0.5rem 0;
            letter-spacing: -1px;
            text-transform: uppercase;
        }
        
        .green-drop-header p {
            font-size: 1.2rem;
            margin: 0;
            opacity: 0.9;
        }
        
        .comparison-table {
            width: 100%;
            border-collapse: collapse;
            background: white;
        }
        
        .plan-header-row {
            background: white;
        }
        
        .plan-header-cell {
            padding: 2rem;
            text-align: center;
            border-bottom: 2px solid #e9ecef;
            position: relative;
            vertical-align: top;
        }
        
        .featured-header {
            background: linear-gradient(180deg, #f0f8ff 0%, white 20%);
            border-left: 3px solid #9fcc3b;
            border-bottom-color: #9fcc3b;
        }
        
        .popular-badge {
            position: absolute;
            top: -10px;
            left: 50%;
            transform: translateX(-50%);
            background: #9fcc3b;
            color: white;
            padding: 5px 15px;
            border-radius: 15px;
            font-size: 0.75rem;
            font-weight: bold;
        }
        
        .plan-name {
            font-family: Arial, sans-serif;
            font-size: 2rem;
            font-weight: bold;
            color: #6151a2;
            margin: 0 0 0.5rem 0;
            text-transform: uppercase;
        }
        
        .plan-tagline {
            font-style: italic;
            color: #666;
            margin: 0 0 1rem 0;
        }
        
        .plan-price {
            font-size: 2.5rem;
            font-weight: bold;
            color: #333;
            margin: 0;
        }
        
        .plan-price .period {
            font-size: 1rem;
            color: #666;
        }
        
        .price-note {
            font-size: 0.8rem;
            color: #888;
            margin-top: 0.5rem;
        }
        
        .section-header {
            background: #6151a2;
            color: white;
            padding: 1rem 1.5rem;
            font-weight: bold;
            font-size: 1.1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            text-align: center;
        }
        
        .section-header.maintenance {
            background: #8b7355;
        }
        
        .feature-cell {
            padding: 1rem 1.5rem;
            border-bottom: 1px solid #e9ecef;
            vertical-align: middle;
            min-height: 60px;
        }
        
        .feature-name {
            background: #f8f9fa;
            font-weight: 500;
            text-align: left;
        }
        
        .feature-value {
            text-align: center;
            font-weight: 500;
        }
        
        .featured-cell {
            background: #f0f8ff;
        }
        
        .checkmark {
            color: #9fcc3b;
            font-size: 1.2rem;
            font-weight: bold;
        }
        
        .x-mark {
            color: #ccc;
            font-size: 1.2rem;
        }
        
        .highlight {
            background: #f0f8ff;
            color: #6151a2;
            font-weight: bold;
            padding: 0.2rem 0.5rem;
            border-radius: 4px;
        }
        
        .premium-feature {
            background: #fff3cd;
            color: #856404;
            font-weight: bold;
            padding: 0.2rem 0.5rem;
            border-radius: 4px;
        }
        
        .cta-cell {
            padding: 2rem 1.5rem;
            text-align: center;
            border-top: 2px solid #e9ecef;
        }
        
        .featured-cta {
            border-top-color: #9fcc3b;
        }
        
        .cta-button {
            background: #9fcc3b;
            color: #333;
            padding: 1rem 2rem;
            border: none;
            border-radius: 6px;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
            transition: all 0.3s ease;
            width: 100%;
            max-width: 200px;
        }
        
        .cta-button:hover {
            background: #8bb82f;
            transform: translateY(-2px);
        }
        
        .featured-button {
            background: #6151a2;
            color: white;
        }
        
        .featured-button:hover {
            background: #5142a2;
        }
        
        .value-props {
            background: #f8f9fa;
            padding: 2rem;
            margin-top: 2rem;
        }
        
        .value-props h2 {
            font-family: Arial, sans-serif;
            font-size: 2rem;
            font-weight: bold;
            color: #6151a2;
            text-align: center;
            margin-bottom: 2rem;
            text-transform: uppercase;
        }
        
        .value-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            max-width: 800px;
            margin: 0 auto;
            justify-content: center;
        }
        
        .value-card {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            flex: 1;
            min-width: 300px;
            max-width: 380px;
        }
        
        .value-card h3 {
            color: #6151a2;
            margin-bottom: 1rem;
            font-size: 1.3rem;
        }
        
        .value-card .tagline {
            font-style: italic;
            color: #9fcc3b;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }
        
        .value-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .value-list li {
            padding: 0.3rem 0;
            position: relative;
            padding-left: 20px;
        }
        
        .value-list li::before {
            content: "•";
            color: #9fcc3b;
            font-weight: bold;
            position: absolute;
            left: 0;
        }
        
        @media (max-width: 768px) {
            .green-drop-container {
                padding: 10px;
            }
            
            .green-drop-header h1 {
                font-size: 2rem;
            }
            
            .comparison-table {
                font-size: 0.9rem;
            }
            
            .plan-header-cell {
                padding: 1rem;
            }
            
            .plan-name {
                font-size: 1.5rem;
            }
            
            .plan-price {
                font-size: 2rem;
            }
            
            .value-grid {
                flex-direction: column;
            }
            
            .value-card {
                min-width: auto;
            }
        }
    </style>
</head>
<body>
    <div class="green-drop-container">
        <div class="green-drop-header">
            <h1>Choose Your Level of Care</h1>
            <p>Two simple options: everything you need, or everything covered</p>
        </div>
        
        <table class="comparison-table">
            <tr class="plan-header-row">
                <td class="plan-header-cell" style="width: 300px;">
                    <div style="font-weight: bold; font-size: 1.5rem; color: #6151a2;">Features</div>
                </td>
                <td class="plan-header-cell">
                    <div class="plan-name">Essential Care</div>
                    <div class="plan-tagline">"Everything you need, nothing you don't"</div>
                    <div class="plan-price">$21<span class="period">/month</span></div>
                    <div class="price-note">*Car Care pricing shown</div>
                </td>
                <td class="plan-header-cell featured-header">
                    <div class="popular-badge">MOST POPULAR</div>
                    <div class="plan-name">Covered Care</div>
                    <div class="plan-tagline">"Your car, completely covered"</div>
                    <div class="plan-price">$49<span class="period">/month</span></div>
                    <div class="price-note">*Car Care pricing shown</div>
                </td>
            </tr>
            
            <!-- Core Maintenance Section -->
            <tr>
                <td class="section-header maintenance">Core Maintenance</td>
                <td class="section-header">✓ All Included</td>
                <td class="section-header">✓ All Included</td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Oil Changes (Full Synthetic)</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Wiper Blade Replacements</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">All Fluid Top-Offs</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Bulb & Fuse Replacements</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Engine & Cabin Air Filters</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Safety Inspections</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Tire Rotations</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Interior Vacuum</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">DEQ Emissions Checks</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <!-- Repair Services Section -->
            <tr>
                <td class="section-header maintenance">Repair Services</td>
                <td class="section-header">✓ All Included</td>
                <td class="section-header">✓ Plus Premium</td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Free Flat Tire Fixes</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Basic Diagnostics</td>
                <td class="feature-cell feature-value"><span class="checkmark">✓</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="checkmark">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Labor Discount</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">10% Off</span></td>
            </tr>
            
            <!-- Premium Benefits Section -->
            <tr>
                <td class="section-header maintenance">Premium Benefits</td>
                <td class="section-header">Select Benefits</td>
                <td class="section-header">✓ All Premium</td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Shop Credit Rewards</td>
                <td class="feature-cell feature-value"><span class="highlight">5%</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">10%</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Winter Tire Swaps</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Car Wash (Per Visit)</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Extended Warranty</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">+1yr/12k</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Green Drop Care+</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">✓</span></td>
            </tr>
            
            <!-- Coverage Protection Section -->
            <tr>
                <td class="section-header maintenance">Coverage Protection</td>
                <td class="section-header">Not Included</td>
                <td class="section-header">✓ Full Coverage</td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Window Repair Coverage</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">✓</span></td>
            </tr>
            
            <tr>
                <td class="feature-cell feature-name">Insurance Deductible Help</td>
                <td class="feature-cell feature-value"><span class="x-mark">—</span></td>
                <td class="feature-cell feature-value featured-cell"><span class="premium-feature">Up to $500</span></td>
            </tr>
            
            <!-- CTA Section -->
            <tr>
                <td class="feature-cell" style="border: none;"></td>
                <td class="cta-cell">
                    <a href="#" class="cta-button">Start Essential Care</a>
                </td>
                <td class="cta-cell featured-cta">
                    <a href="#" class="cta-button featured-button">Start Covered Care</a>
                </td>
            </tr>
        </table>
    </div>

    <div class="value-props">
        <h2>Why Choose Green Drop Membership?</h2>
        <div class="value-grid">
            <div class="value-card">
                <h3>Essential Care</h3>
                <div class="tagline">"Everything you need, nothing you don't"</div>
                <ul class="value-list">
                    <li>Unlimited oil changes & basic maintenance</li>
                    <li>Predictable monthly costs</li>
                    <li>5% shop credit on additional services</li>
                    <li>Perfect for budget-conscious drivers</li>
                    <li>Break-even after just 2 visits</li>
                </ul>
            </div>
            
            <div class="value-card">
                <h3>Covered Care</h3>
                <div class="tagline">"Your car, completely covered"</div>
                <ul class="value-list">
                    <li>Everything in Essential Care PLUS premium benefits</li>
                    <li>10% shop credit + 10% labor discount</li>
                    <li>Winter tire swaps & car washes</li>
                    <li>Extended warranty protection</li>
                    <li>Up to $500 annual deductible coverage</li>
                    <li>True peace of mind driving</li>
                </ul>
            </div>
        </div>
    </div>
</body>
</html>
