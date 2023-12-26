# Ultralytics (CPU) Objekterkennung

Die [YOLO CLI](https://docs.ultralytics.com/quickstart/#use-ultralytics-with-cli) von [Ultralytics](https://ultralytics.com) ermöglicht die bequeme Ausführung der Objekterkennung auf Bildern und Videos.

## Verwendung

Zunächst das Projekt in [GitHub Codespaces](https://codespaces.new/?template_repository=bystefankuehnel/ultralytics) öffnen. Anschließend können die nachfolgenden Schritte ausgeführt werden.

> **Hinweis**: GitHub Codespaces stehen kostenfrei nur für eine begrenzte Zeit (180 Stunden) zur Verfügung. Bei Nichtnutzung sollte ein aktiver Codespace daher gestoppt, bzw. gelöscht werden.

### Schritte

#### 1. Herunterladen eines Videos

Verwendung von `yt-dlp`, um ein Video von YouTube oder einer unterstützten Quelle zu beziehen. Im Beispiel wird ein Video mit dem Namen `cars.mp4` heruntergeladen:

```sh
yt-dlp -o cars.mp4 https://youtu.be/CftLBPI1Ga4
```

> **Hinweis**: Alternativ kann auch ein lokales Video per _Drag & Drop_ hochgeladen werden.

#### 2. Ausführung der YOLO-Objekterkennung

Verwendung von `yolo` zur Ausführung der Objekterkennung für das Video `cars.mp4`:

```sh
yolo predict model=yolov8n-seg.pt source='cars.mp4'
```

> **Hinweis**: Die _annotierte_ Videodatei befindet sich im Ordner `/runs/predict/predict{n}/cars.mp4`.

**Optionen**:

- `model`: Definition des YOLO-Modells zur Objekterkennung. Für Liste der verfügbaren Modelle siehe [hier](https://github.com/ultralytics/ultralytics#models).
- `source`: Definition der Video-Quelle. Kann eine Bild- oder Videodatei sein.
