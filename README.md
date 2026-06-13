# AI-drone-Disease-Detection{
  "system_name": "Agricultural Monitoring Drone for Crop Disease Detection",
  "peas": {
    "performance_measures": [
      "Disease Detection Accuracy",
      "False Alarm Rate",
      "Coverage Area Per Hour",
      "Battery Efficiency",
      "Response Time"
    ],
    "environment": "Large farmland areas containing different crops with weather conditions like sunlight, rain, wind and temperature. Includes different crop growth stages, presence of insects, weeds, plant disease, and obstacles such as trees, buildings, and farming equipment.",
    "actuators": [
      "Flight Control System",
      "Camera Adjustment Mechanism",
      "Spraying System",
      "Communication System"
    ],
    "sensors": [
      "High-Resolution RGB Camera",
      "Infrared/Multi-Spectral Camera",
      "GPS Sensors",
      "Temperature and Humidity Sensor"
    ]
  },
  "environment_classification": {
    "observability": {
      "choice": "Partially Observable",
      "justification": "Drone cannot observe all crop condition because some disease may be hidden under leaves or affected by weather conditions"
    },
    "agents": {
      "choice": "Single Agent",
      "justification": "Drone works as the main decision making agent although it may communicate with farmers or other systems"
    },
    "determinism": {
      "choice": "Stochastic",
      "justification": "Agricultural environment is uncertain because weather changes and disease spread cannot always be predicted accurately"
    },
    "episodicity": {
      "choice": "Sequential",
      "justification": "Each monitoring decision affects future actions such as identifying disease areas and planning future inspections"
    },
    "dynamics": {
      "choice": "Dynamic",
      "justification": "Farming environment changes continuously due to weather, crop growth and disease development"
    },
    "discreteness": {
      "choice": "Continuous",
      "justification": "Drone operates in a continuous environment where location movement temperature and crop condition change continuously"
    }
  },
  "utility_function": "U = 0.6*disease_detection_accuracy + 0.25*coverage_area - 0.15*energy_consumption"
}
