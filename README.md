Whisper STFT / Mel experiments including notebooks and sample audio
Whisper STFT Experiments 🎙️

Whisper 기반 ASR(Automatic Speech Recognition) 실험 노트

오디오 FFT/STFT/Mel Spectrogram 시각화

PySide6 DB 뷰어 및 샘플 오디오 플레이어

📂 Project Structure
WHISPER/
├─ bell.mp3                  # 샘플 오디오 (벨소리)
├─ sample.mp3                # 샘플 오디오 (음성 포함)
├─ stft.ipynb                # STFT/Mel Spectrogram 실험 노트북
└─ SBS_Whisper_Fine-tuning.md(or .ipynb) # Whisper 파인튜닝 기록

🚀 Features

Signal Processing

FFT, STFT 변환 및 주파수 스펙트럼 시각화

Mel Spectrogram 변환 및 dB 스케일 시각화

ASR Pipeline

Whisper Feature Extractor / Tokenizer 활용

한국어 음성 전사 실험

Visualization

librosa, torchaudio 기반 시각화

PySide6/Qt GUI로 DB 데이터 및 스크립트 뷰어 제작

Experiment Tracking

W&B(Weights & Biases) 연동 가능

CER(Character Error Rate) 기반 성능 비교

🔧 Installation

프로젝트는 uv 환경 매니저를 기준으로 합니다.

# 의존성 설치
uv sync

# 주요 패키지 수동 설치 (필요시)
uv add pandas pymysql PySide6 librosa torchaudio transformers jiwer wandb

🧪 Usage
1) Jupyter Notebook
uv run jupyter lab


stft.ipynb 실행 → FFT/STFT/Mel Spectrogram 시각화 확인 가능

2) PySide6 뷰어
uv run python main.py


DB에서 불러온 스크립트 비교

오디오 파일 선택 & 재생

match/mismatch 결과를 Pie/Bar Chart로 시각화

📊 Example Results
Spectrogram Example

(샘플 오디오 bell.mp3 변환 예시)

Mel Spectrogram Example

(사람 음성과 벨소리 주파수 비교)

📝 Notes

Whisper 모델은 Hugging Face Transformers 기반

실험용 데이터셋은 SBS ASR DB와 로컬 샘플(bell.mp3, sample.mp3) 사용

민감 데이터(sbs_datasets/, sbs_datasets_processed/)는 .gitignore로 제외

📌 To-do

 Whisper fine-tuning 결과 정리 업로드

 CER 계산/평가 스크립트 추가

 Redis/RQ 큐 기반 데이터 처리 예제 포함

📜 License

MIT License
(※ 사내 데이터/DB 관련 부분은 공유하지 마세요)
