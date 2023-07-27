# DocumentReference

The DocumentReference endpoint is used to read and write general documents, PDFs, attachments, and other notes related to Ocean.

This resource may be returned in the $everything Bundle, particularly to hold a user's pre-selected note with an attachment as part of a contextual launch. For example, a user may select an ultrasound report, then initiate a contextual launch (SMART on FHIR) or trigger a patient upload via the Ocean portal. From here, Ocean will call the $everything operation and will receive the note and the ultrasound PDF as a DocumentReference. See the $everything operation definition in this project for details.

Ocean expects the "title" of the DocumentReference.attachment.content to be a file name with a supported extension. Valid extensions include but may not be limited to: "jpg", "jpeg", "png", "tiff", "tif", "bmp", "mp3", "mp4", "txt", "pdf", "mov", "avi"
