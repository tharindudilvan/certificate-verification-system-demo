# certificate-verification-system-demo
Project demo and documentation for a blockchain-based certificate verification system

# 🔐 Secure Certificate Verification System

A modern web-based system for issuing, managing, and verifying academic certificates using **blockchain-inspired integrity verification**.

---

## 🚀 Project Overview

This system allows institutions to:
- Issue digital certificates
- Verify certificates publicly using Certificate ID or QR code
- Detect tampering using cryptographic hashing
- Maintain a blockchain-style ledger for integrity

---

## 🎯 Key Features

### 🔑 Admin Panel
- Secure login (bcrypt authentication)
- Manage students (add, edit, delete, search)
- Issue certificates
- Edit, revoke, and delete certificates

### 📜 Certificate System
- Unique Certificate ID
- PDF certificate generation
- QR code generation for quick verification
- Certificate status (Valid / Revoked)

### 🔍 Public Verification
- Verify certificate using Certificate ID
- QR-based verification
- Displays:
  - student details
  - course
  - issue date
  - certificate status

### 🔗 Blockchain Integrity Layer
- SHA-256 hash generation for each certificate
- Blockchain-style ledger storage
- Tamper detection using hash recalculation
- Verification result:
  - ✅ Verified
  - ❌ Not Verified (Tampering Detected)

---

## 🧠 How Tamper Detection Works

1. Certificate data → hashed (SHA-256)
2. Hash stored in database + blockchain ledger
3. During verification:
   - System recalculates hash from current data
   - Compares with blockchain hash

If mismatch:

