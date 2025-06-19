# InkSentinel: AI-Powered Handwritten Signature Verification

InkSentinel is a cutting-edge mobile application leveraging advanced artificial intelligence to verify handwritten signatures with forensic-level precision. Tailored for industries prone to fraud, such as banking, legal services, and education, InkSentinel achieves over 90% accuracy in under 30 milliseconds, surpassing traditional verification methods.

---

## Key Features

- **⚡ Lightning-Fast Verification**  
  Achieves 90.83% accuracy in <30ms using Siamese Neural Networks with EfficientNet-Lite.

- **📱 Multi-Platform Support**  
  Native iOS and Android apps developed with Flutter for a seamless user experience.

- **🗣️ Bilingual AI Assistant**  
  Provides real-time forensic guidance in English and Arabic, powered by Ollama's LLaMA3.2:latest.

- **🔒 Military-Grade Security**  
  Implements AES-256 encryption, GDPR compliance, and Firebase authentication.

- **🌐 Offline Capability**  
  TorchScript-optimized model enables verification without internet (<200ms inference).

- **📊 Dynamic Analytics**  
  Offers verification history with search/filter options and visual similarity reports.

---

## Technologies Used

### Core Stack
- **Frontend**: Flutter
- **Backend**: Python, Flask
- **AI/ML**: PyTorch, Ollama
- **Database & Auth**: Firebase

### AI Models
- **Signature Verification**: Siamese Network with EfficientNet-Lite0
- **Chatbot**: Meta's LLaMA3.2:latest (3B parameter LLM)

### Security
- AES-256 Encryption
- Firebase Authentication
- Role-Based Access Control
- GDPR Compliance

---

## Installation & Setup

### Mobile Application (Android)
1. **Download APK**  
   Get the latest release from [GitHub Releases](https://github.com/graduationteam25/InkSentinel/releases).

2. **Enable Unknown Sources**  
   Navigate to `Settings → Security → Enable "Install unknown apps"`.

3. **Install & Launch**  
   Open the APK file and follow the installation prompts.

### Development Environment
1. **Clone the Repository**
   ```bash
   git clone https://github.com/graduationteam25/InkSentinel
   ```

2. **Install Flutter Dependencies**
   ```bash
   cd inksentinel
   flutter pub get
   ```

3. **Run the Flutter App**
   ```bash
   flutter run
   ```

4. **Start the Backend Server**
   ```bash
   cd API_model
   pip install -r requirements.txt
   python app.py
   ```

---

## Dataset

InkSentinel's AI model was trained on the **CEDAR Signature Verification Dataset**.  
- **Download**: [CEDAR Dataset](https://cedar.buffalo.edu/resources.html)  
- **Structure**:
  ```
  ├── original
  │   ├── original_1.png
  │   └── ...
  └── forged
      ├── forged_1.png
      └── ...
  ```

---

## Chatbot Integration

The bilingual assistant runs locally using the **Ollama Framework**. Below is a sample API call:

```python
import ollama

response = ollama.chat(
    model='llama3.2:latest',
    messages=[{'role': 'user', 'content': 'Explain signature forgery types'}]
)
print(response['message']['content'])
```

---

## Future Roadmap

- **Accuracy Boost**: Target 95%+ with ensemble models.
- **Liveness Detection**: Prevent screenshot spoofing.
- **Blockchain Integration**: Immutable verification records.
- **Enterprise API**: RESTful service for document workflows.
- **Cross-Platform Expansion**: Web and desktop versions.
- **Multi-Signature Analysis**: Support for contract verification.

---

## Contributing

We welcome contributions! Please check out our [GitHub repository](https://github.com/graduationteam25/InkSentinel) to get started.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

**GitHub Repository**: [graduationteam25/InkSentinel](https://github.com/graduationteam25/InkSentinel)
