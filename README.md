# UrbanSenseAI

**UrbanSenseAI** is an agentic AI mobile application designed for the IBM Call for Code 2025 challenge, aligning with UN SDG 11: Sustainable Cities and Communities. It empowers visually impaired individuals to navigate urban environments independently by providing real-time audio descriptions of surroundings using a smartphone camera, powered by IBM watsonx. The app assists with tasks like identifying bus numbers, crossing roads safely, locating shops, and accessible wayfinding.

## Project Overview
UrbanSenseAI leverages IBM watsonx to deploy autonomous AI agents that process live video from a smartphone camera, integrate contextual data (e.g., GPS, transit schedules), and deliver audio feedback. The solution enhances accessibility and safety in cities, supporting SDG 11’s goals of inclusive transport (Target 11.2) and public spaces (Target 11.7).

### Key Features
- **Bus Identification**: Detects bus numbers and destinations, confirming the correct bus via transit APIs.
- **Road Crossing Assistance**: Analyzes pedestrian signals and traffic to guide safe crossing.
- **Shop Localization**: Identifies shops or landmarks by name using image recognition and GPS.
- **Accessible Wayfinding**: Generates audio-based, accessible walking routes.
- **Environmental Awareness**: Provides real-time audio descriptions of surroundings.
- **Emergency Support**: Offers immediate guidance in unsafe situations.

### User Workflows
1. **Boarding the Correct Bus**: Detects bus numbers and verifies routes via audio (e.g., “Bus 42 to Downtown, 10 meters away”).
2. **Safe Road Crossing**: Alerts users to pedestrian signals and hazards (e.g., “Green light, safe to cross”).
3. **Locating Shops**: Finds shops by name or type (e.g., “Starbucks 50 meters right”).
4. **Accessible Navigation**: Guides users to destinations with accessible routes.
5. **Environmental Exploration**: Describes surroundings for situational awareness.
6. **Emergency Assistance**: Provides location-based guidance in unsafe scenarios.

## Technical Architecture
- **Frontend**: Mobile app (iOS/Android) with voice-activated controls and haptic feedback.
- **Backend**: IBM watsonx platform:
  - **Watsonx.ai**: Computer vision for object detection (e.g., buses, traffic lights) and OCR for text recognition.
  - **Watsonx.data**: Integrates GPS, OpenStreetMap, and transit APIs (e.g., GTFS).
  - **Watsonx Assistant**: Handles voice input and text-to-speech audio output.
- **Data Sources**: Smartphone camera (live video), OpenStreetMap, GTFS transit feeds, GPS.
- **Agents**:
  - Vision Agent: Detects objects and text.
  - Context Agent: Integrates location and transit data.
  - Safety Agent: Monitors hazards.
  - Navigation Agent: Generates accessible routes.
  - Communication Agent: Delivers audio feedback.

## Installation
### Prerequisites
- Node.js (v16+)
- Python (3.8+)
- IBM Cloud account with access to Watsonx.ai, Watsonx.data, and Watsonx Assistant
- Mobile development environment (e.g., React Native, Flutter)
- OpenStreetMap API key (optional for map data)
- GTFS feed access for transit data (optional)

### Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-team/UrbanSenseAI.git
   cd UrbanSenseAI
   ```
2. **Install Dependencies**:
   ```bash
   npm install  # For frontend (e.g., React Native)
   pip install -r requirements.txt  # For backend scripts
   ```
3. **Configure IBM Watsonx**:
   - Set up an IBM Cloud account and provision Watsonx.ai, Watsonx.data, and Watsonx Assistant services.
   - Add API keys to `.env` file (see `.env.example`).
4. **Configure Data Sources**:
   - Download OpenStreetMap data for your test city.
   - Obtain GTFS feed for transit schedules (e.g., from local transit authority).
5. **Run the App**:
   ```bash
   npm start  # Start frontend (React Native/Flutter)
   python backend/main.py  # Start backend (if separate)
   ```
6. **Test the App**:
   - Use pre-recorded urban videos or live camera feed for testing.
   - Simulate workflows (e.g., bus detection, road crossing) on a mid-range smartphone.

## Development Status
This project is a proof-of-concept (POC) for IBM Call for Code 2025. Current focus:
- Implementing Workflows 1 (Bus Identification) and 2 (Road Crossing).
- Using lightweight vision models (e.g., MobileNet, Tesseract OCR) for real-time performance.
- Integrating Watsonx Assistant for voice input/output.
- Testing with simulated urban data (e.g., OpenStreetMap, GTFS).

## Contributing
We welcome contributions! Please follow these steps:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit changes (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License
This project is licensed under the MIT License. See `LICENSE` for details.

## Contact
For questions or feedback, reach out to [your-team-email@example.com] or open an issue on GitHub.

## Acknowledgments
- IBM Call for Code for providing the platform and Watsonx tools.
- OpenStreetMap and GTFS communities for open data.
- Visually impaired communities for inspiring this inclusive solution.