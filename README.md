 ##  ekg_waveforms

**ekg_waveforms** is a modular Python toolkit for processing and visualizing ECG signals from the MIT-BIH Arrhythmia Database. It enables conversion of `.dat` files to `.csv`, waveform plotting with R-peak and QRS complex annotations, normalization for clear visuals, and export to `.png`. Includes CLI interface and modular structure for easy extension.

---

##  Features

-  Batch convert MIT-BIH `.dat` ECG records to `.csv`
-  Plot ECG signals from `.csv` with:
  -> R-peak detection
  -> QRS complex highlights (coming soon)
  -> Optional signal normalization
-  Save waveform plots as `.png`
-  CLI interface for easy automation
-  (Optional) GUI with Tkinter (coming soon)
-  Clean modular design: easy to extend with more features

---

## 🗂 Folder Structure

    ekg_waveforms/
    ├── mitdb/ # Input .dat, .hea, .atr files
    ├── data/ # Output folder for .csv and plots
    ├── convert.py # Converts .dat → .csv
    ├── plot.py # Plots ECG waveform from .csv
    ├── utils.py # Helper functions (normalization, etc.)
    ├── cli.py # Command-line interface
    ├── gui.py # GUI frontend (optional)
    ├── main.py # Entry point script
    ├── requirements.txt # Python dependencies
    └── README.md # Documentation



---

## ⚙️ Installation

Clone the repo and install dependencies:

  ```
git clone https://github.com/yourusername/ekg_waveforms.git
cd ekg_waveforms
pip install -r requirements.txt

```

##🚀 Usage
🛠 Convert MIT-BIH `.dat` to `.csv`

     python cli.py convert --src mitdb/ --dest data/

Converts all `.dat` files from `mitdb/` to `.csv` in the `data/` folder.

 Plot ECG from CSV:

    python cli.py plot --file data/100.csv --save data/100_plot.png --normalize
    
CLI Flags:
--file: Path to the .csv file

--save: (Optional) Path to save the plot as .png

--normalize: (Optional) Normalize signal amplitude for display

--no-annotate: (Optional) Disable R-peak annotation

 Run GUI (coming soon)

    python gui.py

 Requirements
Install via:


    pip install -r requirements.txt



Dependencies include:

- pandas

- matplotlib

- wfdb

 Sample Output


markdown

     ![Sample ECG](data/sample_ecg_plot.png)

🧠 Credits
- [MIT-BIH Arrhythmia Database](https://physionet.org/content/mitdb/1.0.0/)
- Built using the [WFDB Python Toolkit](https://github.com/MIT-LCP/wfdb-python)


📜 License
This project is licensed under the `MIT License`.

🤝 Contributing
Contributions, feature suggestions, and PRs are welcome!

Fork this repo

Create your feature branch: `git checkout -b feature/new-feature`

Commit your changes: git commit `-m 'Add feature'`

Push to the branch: `git push origin feature/new-feature`

Open a pull request 🎉


---


