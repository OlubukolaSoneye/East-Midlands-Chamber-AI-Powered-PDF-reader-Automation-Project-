Python Code

import os
import fitz  # PyMuPDF


def setup_folders():
    """Create necessary folders if they don't exist"""
    folders = {
        'input': 'pdf_files',
        'output': 'converted_images'
    }

    for folder in folders.values():
        if not os.path.exists(folder):
            os.makedirs(folder)
            print(f"Created folder: {folder}")

    return folders


def convert_pdf(pdf_path, output_folder):
    """Convert a single PDF to images"""
    try:
        doc = fitz.open(pdf_path)
        filename = os.path.basename(pdf_path).replace('.pdf', '')

        for page_num in range(len(doc)):
            page = doc.load_page(page_num)
            image = page.get_pixmap(dpi=150)
            image.save(f"{output_folder}/{filename}_page{page_num + 1}.png")

        print(f"Converted: {filename} ({len(doc)} pages)")
        return True

    except Exception as e:
        print(f"Failed to convert {pdf_path}: {str(e)}")
        return False


def main():
    # Setup folders in current directory
    folders = setup_folders()

    # Get all PDF files
    pdf_files = [f for f in os.listdir(folders['input'])
                 if f.lower().endswith('.pdf')]

    if not pdf_files:
        print(f"\nNo PDF files found in '{folders['input']}' folder")
        print("Please add PDF files and try again")
        return

    print(f"\nFound {len(pdf_files)} PDF(s) to convert")

    # Process each PDF
    success_count = 0
    for pdf_file in pdf_files:
        pdf_path = os.path.join(folders['input'], pdf_file)
        if convert_pdf(pdf_path, folders['output']):
            success_count += 1

    # Results summary
    print(f"\nConversion complete!")
    print(f"Successful: {success_count}")
    print(f"Failed: {len(pdf_files) - success_count}")
    print(f"\nImages saved in: {folders['output']}")


if __name__ == "__main__":
    print("PDF to Image Converter")
    print("=" * 40)
    main()
                                                                     

 
