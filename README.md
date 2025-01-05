# Refinamento-da-Solu-o-Inicial
# 7.2. Etapa Consolidar - Refinamento da Solução Inicial
import cv2
import os

def main():
    # Caminho absoluto para o arquivo de vídeo
    video_path = r"C:\Users\tocac\PycharmProjects\Rastreamento_dense\walking.avi"
    cap = cv2.VideoCapture(video_path)

    if not cap.isOpened():
        print("Erro ao abrir o arquivo de vídeo.")
        return

    print("Arquivo de vídeo aberto com sucesso!")

    while True:
        ret, frame = cap.read()
        if not ret:
            break

        # Exibir o frame do vídeo original
        cv2.imshow('Video Original', frame)

        if cv2.waitKey(1) == 13:  # Enter key to stop
            break

    cap.release()
    cv2.destroyAllWindows()

if __name__ == "__main__":
    main()
