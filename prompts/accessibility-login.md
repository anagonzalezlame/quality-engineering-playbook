# 🤖 GenAI Prompts: Accessibility (A11y) for Login Forms

Use these prompts to accelerate the creation of accessibility test cases, ensuring compliance with **WCAG 2.1/2.2 (Level AA)**.

---

## Prompt 1: Comprehensive Test Case Generation
> **Role:** Senior QA Accessibility Specialist.
> **Context:** Testing a standard Login Form (Email, Password, Remember Me, Submit).
> **Task:** Generate a detailed test suite focused on Screen Readers and Keyboard Navigation.
> **Format:** Table including: Test ID, Requirement, Step, Expected Result, and WCAG Criterion.

## Prompt 2: ARIA Attributes Validation
> **Task:** Act as an Accessibility Auditor. Review the following HTML snippet for a Login Button and identify missing or incorrect ARIA attributes. Suggest the corrected code for:
> 1. Error message association (aria-describedby).
> 2. Loading states (aria-busy).
> 3. Field requirements (aria-required).

## Prompt 3: Color Contrast & Visual Cues
> **Context:** A login form with a #007bff (Blue) primary button on a white background and red error text.
> **Task:** > 1. Verify if the contrast ratio meets WCAG AA standards.
> 2. Suggest 3 alternative ways to communicate "Error" that do not rely solely on color (e.g., icons, text patterns).

## Prompt 4: Focus Order & Trap Management
> **Task:** Create a test script for "Keyboard Trap" detection in a Login Modal. 
> **Instructions:** Include steps to verify focus trapping within the modal, the logical tab order (Email -> Password -> Login), and the escape key functionality to close the modal.
