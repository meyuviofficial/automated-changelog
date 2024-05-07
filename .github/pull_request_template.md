## Pull Request Template: Custom Golden Image with Ansible, Packer, and Terraform

**Type of Change:** [**New Feature** | **Bug Fix** | **Improvement** | **Other (Specify)**]

**Title:** Implement Custom Golden Image with [**Description of Image**] ([#PR number])

**Description:**

This pull request introduces a new golden image build process utilizing Ansible, Packer, and Terraform. The image caters to [**Target audience/use case**] within the enterprise.

**Changes Introduced:**

* **Terraform:**
    * New Terraform configuration files (`[directory]/terraform/*`) define the infrastructure for building the image (e.g., cloud provider resources, credentials).
    * Update `[main.tf]` or a dedicated file to provision the build environment (builder instance).
* **Packer:**
    * Packer template (`[directory]/packer.json`) defines the build process for the golden image.
    * The template utilizes Ansible playbooks for image customization.
* **Ansible:**
    * Playbooks (`[directory]/ansible/playbooks/*`) configure the golden image using Ansible modules.
    * Roles (`[directory]/ansible/roles/*`) (optional) can be used for modular code organization.
    * Inventory file (`[directory]/ansible/inventory`) defines the target machine (builder instance) for playbook execution.
* **Documentation (Optional):**
    * Update documentation ([link to documentation]) to reflect the new image build process and usage instructions.

**Testing:**

* Manual testing of the image build process is recommended.
* (Optional) Define automated tests (e.g., unit tests, integration tests) to ensure image build consistency.

**Review Points:**

* Code clarity and maintainability of Terraform, Packer, and Ansible configurations.
* Security considerations within the image build process and final image.
* Documentation updates for clarity and ease of use by the target audience.

**Additional Notes:**

* Mention any specific dependencies or configurations needed for running the build process.
* Consider including a sample `Makefile` or script to automate the build process execution.


**Please review the changes and provide feedback.**

**Approvers:**

* Infrastructure team lead
* Security team representative (if applicable)

**Once approved, this pull request will enable the creation and distribution of the custom golden image for wider enterprise usage.**
